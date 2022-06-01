# Sidorov Aleksey

### Contacts:

* Tel: +7-999-608-36-63
* eMail: alekseysidorov.28@gmail.com
* Telegram: @tararatel
* Discord: Aleksey Sidorov#0427

### About myself:

I graduated from GeekBrains University at the faculty of frontend.

** ### Skills: **

* HTML
* CSS
* JavaScript
* TypeScript
* React
* Next.js
* Vue.js
* SCRUM
* Nest.js

### Code example:

` ` `

function TopPage({ firstCategory, page, products }: TopPageProps): JSX.Element {
	if (!page || !products) {
		return <Error404 />;
	}
	return (
		<>
			<Head>
				<title>{page.metaTitle}</title>
				<meta name="description" content={page.metaDescription} />
				<meta property="og:title" content={page.metaTitle} />
				<meta property="og:description" content={page.metaDescription} />
				<meta property="og:type" content="article" />
			</Head>
			<TopPageComponent firstCategory={firstCategory} page={page} products={products} />
		</>
	);
}

export default withLayout(TopPage);

export const getStaticPaths: GetStaticPaths = async () => {
	let paths: string[] = [];
	for (const m of firstLevelMenu) {
		const { data: menu } = await axios.post<MenuItem[]>(API.topPage.find, {
			firstCategory: m.id,
		});
		paths = paths.concat(menu.flatMap((s) => s.pages.map((p) => `/${m.route}/${p.alias}`)));
	}

	return {
		paths,
		fallback: false,
	};
};

` ` `

### Work experience:

1. 3 Web-приложения на Vue 3
* https://github.com/Tararatel/vue3-notify ( Демо-версия проекта - https://clck.ru/gwExy )
* https://github.com/Tararatel/vue3-clash-of-clans ( Демо-версия проекта - https://clck.ru/gwDgH )
* https://github.com/Tararatel/vue3_ts-star_wars ( Демо-версия проекта - https://clck.ru/gwEtb )
2. Web-приложение на Next.js
* https://github.com/Tararatel/Next.js_TS_Hooks_SSR ( Демо-версия проекта - https://clck.ru/gwD2K )

### Education and courses:
* GekkBrains University - https://gb.ru/
* React + Next.js - с нуля. TypeScript, Hooks, SSR и CSS Grid - https://learn.purpleschool.ru/
* NestJS - с нуля, современный backend на TypeScript и Node JS - https://www.udemy.com/

## Language:
English level - Intermediate
