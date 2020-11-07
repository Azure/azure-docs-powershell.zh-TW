---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 477b60400082954eb12bd0756fb4380ece2a35ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794986"
---
# <span data-ttu-id="a92ff-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a92ff-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="a92ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a92ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a92ff-103">取得 Azure Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="a92ff-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="a92ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="a92ff-104">SYNTAX</span></span>

### <span data-ttu-id="a92ff-105">S1</span><span class="sxs-lookup"><span data-stu-id="a92ff-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a92ff-106">S2</span><span class="sxs-lookup"><span data-stu-id="a92ff-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a92ff-107">說明</span><span class="sxs-lookup"><span data-stu-id="a92ff-107">DESCRIPTION</span></span>
<span data-ttu-id="a92ff-108">**AzWebAppPublishingProfile** Cmdlet 會取得 Azure Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="a92ff-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="a92ff-109">示例</span><span class="sxs-lookup"><span data-stu-id="a92ff-109">EXAMPLES</span></span>

### <span data-ttu-id="a92ff-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="a92ff-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="a92ff-111">這個命令會針對與資源群組預設-Web WestUS 相關聯的 Web App ContosoWebApp，取得 Ftp 格式的發佈設定檔，並將它儲存在指定的輸出檔案中。</span><span class="sxs-lookup"><span data-stu-id="a92ff-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="a92ff-112">參數</span><span class="sxs-lookup"><span data-stu-id="a92ff-112">PARAMETERS</span></span>

### <span data-ttu-id="a92ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92ff-113">-DefaultProfile</span></span>
<span data-ttu-id="a92ff-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a92ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92ff-115">-Format</span><span class="sxs-lookup"><span data-stu-id="a92ff-115">-Format</span></span>
<span data-ttu-id="a92ff-116">設置</span><span class="sxs-lookup"><span data-stu-id="a92ff-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92ff-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a92ff-117">-Name</span></span>
<span data-ttu-id="a92ff-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="a92ff-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92ff-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="a92ff-119">-OutputFile</span></span>
<span data-ttu-id="a92ff-120">輸出檔案</span><span class="sxs-lookup"><span data-stu-id="a92ff-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92ff-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92ff-121">-ResourceGroupName</span></span>
<span data-ttu-id="a92ff-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a92ff-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92ff-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a92ff-123">-WebApp</span></span>
<span data-ttu-id="a92ff-124">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="a92ff-124">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a92ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92ff-125">CommonParameters</span></span>
<span data-ttu-id="a92ff-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a92ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92ff-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a92ff-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92ff-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a92ff-128">INPUTS</span></span>

### <span data-ttu-id="a92ff-129">網站地圖</span><span class="sxs-lookup"><span data-stu-id="a92ff-129">Site</span></span>
<span data-ttu-id="a92ff-130">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a92ff-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a92ff-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a92ff-131">OUTPUTS</span></span>

## <span data-ttu-id="a92ff-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a92ff-132">NOTES</span></span>

## <span data-ttu-id="a92ff-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a92ff-133">RELATED LINKS</span></span>

[<span data-ttu-id="a92ff-134">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a92ff-134">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="a92ff-135">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a92ff-135">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

