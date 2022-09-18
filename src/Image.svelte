<script>
    import src from './assets/profile.webp';
    const name = "Krzysztof Królikowski";

    const zipCode = (code, location) => {
        // let _code = code;
        // let _location = location;

        return ({
          code: () => code,
          location: () => location,
        })
    }

    let obj = {abc: 'test'}
    const princetonZip = zipCode(obj, '3345');
    console.log(princetonZip.code(), "codeBeforeChange")

    obj = {hej: "mała"}

    console.log(princetonZip.code(), "codeAfterChange")
</script>

<!--{JSON.stringify(princetonZip)}-->
<!--{JSON.stringify(princetonZip.code())}-->
<!--{JSON.stringify(princetonZip.location())}-->
<img {src} alt="A {name} dances" class="image">

<style>
    .image {
        border-radius: 50%;
    }
    .image:hover {
        filter: drop-shadow(0 0 2em #888);
    }
</style>
