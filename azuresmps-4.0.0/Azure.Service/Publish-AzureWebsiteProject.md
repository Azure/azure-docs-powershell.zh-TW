---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967323"
---
# <span data-ttu-id="d08db-101">Publish-AzureWebsiteProject</span><span class="sxs-lookup"><span data-stu-id="d08db-101">Publish-AzureWebsiteProject</span></span>

## <span data-ttu-id="d08db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d08db-102">SYNOPSIS</span></span>
<span data-ttu-id="d08db-103">使用 WebDeploy 將 Visual Studio Web 專案發佈到 Microsoft Azure 網站。</span><span class="sxs-lookup"><span data-stu-id="d08db-103">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>

## <span data-ttu-id="d08db-104">句法</span><span class="sxs-lookup"><span data-stu-id="d08db-104">SYNTAX</span></span>

### <span data-ttu-id="d08db-105">ProjectFile</span><span class="sxs-lookup"><span data-stu-id="d08db-105">ProjectFile</span></span>
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d08db-106">套件</span><span class="sxs-lookup"><span data-stu-id="d08db-106">Package</span></span>
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d08db-107">說明</span><span class="sxs-lookup"><span data-stu-id="d08db-107">DESCRIPTION</span></span>
<span data-ttu-id="d08db-108">使用 WebDeploy 將 Visual Studio Web 專案發佈到 Microsoft Azure 網站。</span><span class="sxs-lookup"><span data-stu-id="d08db-108">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>
<span data-ttu-id="d08db-109">它可以採用 WebDeploy 套件並直接發佈，或是拍攝 Visual Studio Web 專案、建立專案併發布。</span><span class="sxs-lookup"><span data-stu-id="d08db-109">It can either take a WebDeploy package and publish directly, or take a Visual Studio web project, build the project and publish.</span></span>
<span data-ttu-id="d08db-110">在發佈期間，它也可以取代 Web.config 中的連線字串。</span><span class="sxs-lookup"><span data-stu-id="d08db-110">It can also replace the connection strings in the Web.config during publish.</span></span>

## <span data-ttu-id="d08db-111">示例</span><span class="sxs-lookup"><span data-stu-id="d08db-111">EXAMPLES</span></span>

### <span data-ttu-id="d08db-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d08db-112">Example 1</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

<span data-ttu-id="d08db-113">建立具有「調試」設定的 Visual Studio Web 專案 (意思是使用 Web.Debug.config) 並使用 WebDeploy 發佈到 Microsoft Azure 網站。</span><span class="sxs-lookup"><span data-stu-id="d08db-113">Build a Visual Studio web project with "Debug" configuration (meaning use Web.Debug.config) and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="d08db-114">範例2</span><span class="sxs-lookup"><span data-stu-id="d08db-114">Example 2</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

<span data-ttu-id="d08db-115">使用 WebDeploy 將 WebDeploy 套件 .zip 檔案發佈至 Microsoft Azure 網站。</span><span class="sxs-lookup"><span data-stu-id="d08db-115">Publish a WebDeploy Package .zip file to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="d08db-116">範例3</span><span class="sxs-lookup"><span data-stu-id="d08db-116">Example 3</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

<span data-ttu-id="d08db-117">使用 WebDeploy 將 WebDeploy 套件資料夾發佈至 Microsoft Azure 網站。</span><span class="sxs-lookup"><span data-stu-id="d08db-117">Publish a WebDeploy Package folder to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="d08db-118">範例4</span><span class="sxs-lookup"><span data-stu-id="d08db-118">Example 4</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

<span data-ttu-id="d08db-119">建立 Visual Studio Web 專案，在 Web.config 中覆寫 [DefaultConnection] 連線字串，然後使用 WebDeploy 發佈到 Microsoft Azure 網站。</span><span class="sxs-lookup"><span data-stu-id="d08db-119">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="d08db-120">範例5</span><span class="sxs-lookup"><span data-stu-id="d08db-120">Example 5</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

<span data-ttu-id="d08db-121">建立 Visual Studio Web 專案，在 Web.config 中覆寫 [DefaultConnection] 連線字串，然後使用 WebDeploy 發佈到 Microsoft Azure 網站。</span><span class="sxs-lookup"><span data-stu-id="d08db-121">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>
<span data-ttu-id="d08db-122">請注意，-DefaultConnection 是一個由分析 Web.config 新增的動態參數。</span><span class="sxs-lookup"><span data-stu-id="d08db-122">Notice that -DefaultConnection is a dynamic parameter which gets added by parsing Web.config.</span></span>

## <span data-ttu-id="d08db-123">參數</span><span class="sxs-lookup"><span data-stu-id="d08db-123">PARAMETERS</span></span>

### <span data-ttu-id="d08db-124">-配置</span><span class="sxs-lookup"><span data-stu-id="d08db-124">-Configuration</span></span>
<span data-ttu-id="d08db-125">用來建立 Visual Studio web 應用程式專案的配置。</span><span class="sxs-lookup"><span data-stu-id="d08db-125">The configuration used to build the Visual Studio web application project.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08db-126">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d08db-126">-ConnectionString</span></span>
<span data-ttu-id="d08db-127">要用於部署的連接字串。</span><span class="sxs-lookup"><span data-stu-id="d08db-127">The connection strings to use for the deployment.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08db-128">-DoNotDelete</span><span class="sxs-lookup"><span data-stu-id="d08db-128">-DoNotDelete</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08db-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="d08db-129">-Name</span></span>
<span data-ttu-id="d08db-130">網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="d08db-130">The web site name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08db-131">-套件</span><span class="sxs-lookup"><span data-stu-id="d08db-131">-Package</span></span>
<span data-ttu-id="d08db-132">要發佈之 Visual Studio web 應用程式專案之 zip 檔案的 [WebDeploy 套件] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="d08db-132">The WebDeploy package folder for zip file of the Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08db-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d08db-133">-Profile</span></span>
<span data-ttu-id="d08db-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d08db-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d08db-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d08db-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08db-136">-ProjectFile</span><span class="sxs-lookup"><span data-stu-id="d08db-136">-ProjectFile</span></span>
<span data-ttu-id="d08db-137">要發佈的 Visual Studio web 應用程式專案。</span><span class="sxs-lookup"><span data-stu-id="d08db-137">The Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08db-138">-SetParametersFile</span><span class="sxs-lookup"><span data-stu-id="d08db-138">-SetParametersFile</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08db-139">-SkipAppData</span><span class="sxs-lookup"><span data-stu-id="d08db-139">-SkipAppData</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08db-140">-槽</span><span class="sxs-lookup"><span data-stu-id="d08db-140">-Slot</span></span>
<span data-ttu-id="d08db-141">網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="d08db-141">The web site slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08db-142">-標記</span><span class="sxs-lookup"><span data-stu-id="d08db-142">-Tokens</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08db-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08db-143">CommonParameters</span></span>
<span data-ttu-id="d08db-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d08db-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08db-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d08db-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08db-146">輸入</span><span class="sxs-lookup"><span data-stu-id="d08db-146">INPUTS</span></span>

## <span data-ttu-id="d08db-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d08db-147">OUTPUTS</span></span>

## <span data-ttu-id="d08db-148">筆記</span><span class="sxs-lookup"><span data-stu-id="d08db-148">NOTES</span></span>

## <span data-ttu-id="d08db-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="d08db-149">RELATED LINKS</span></span>

[<span data-ttu-id="d08db-150">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d08db-150">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="d08db-151">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d08db-151">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="d08db-152">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d08db-152">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="d08db-153">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d08db-153">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


