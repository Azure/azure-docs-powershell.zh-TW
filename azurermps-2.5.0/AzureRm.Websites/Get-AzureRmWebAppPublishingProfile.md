---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: 5884092a7520517844d6d0137023f99dc744cb86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800257"
---
# <span data-ttu-id="de306-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="de306-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="de306-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de306-102">SYNOPSIS</span></span>
<span data-ttu-id="de306-103">取得 Azure Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="de306-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de306-104">句法</span><span class="sxs-lookup"><span data-stu-id="de306-104">SYNTAX</span></span>

### <span data-ttu-id="de306-105">S1</span><span class="sxs-lookup"><span data-stu-id="de306-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de306-106">S2</span><span class="sxs-lookup"><span data-stu-id="de306-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de306-107">說明</span><span class="sxs-lookup"><span data-stu-id="de306-107">DESCRIPTION</span></span>
<span data-ttu-id="de306-108">**AzureRmWebAppPublishingProfile** Cmdlet 會取得 Azure Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="de306-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="de306-109">示例</span><span class="sxs-lookup"><span data-stu-id="de306-109">EXAMPLES</span></span>

### <span data-ttu-id="de306-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="de306-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="de306-111">這個命令會針對與資源群組預設-Web WestUS 相關聯的 Web App ContosoWebApp，取得 Ftp 格式的發佈設定檔，並將它儲存在指定的輸出檔案中。</span><span class="sxs-lookup"><span data-stu-id="de306-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="de306-112">參數</span><span class="sxs-lookup"><span data-stu-id="de306-112">PARAMETERS</span></span>

### <span data-ttu-id="de306-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de306-113">-DefaultProfile</span></span>
<span data-ttu-id="de306-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de306-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de306-115">-Format</span><span class="sxs-lookup"><span data-stu-id="de306-115">-Format</span></span>
<span data-ttu-id="de306-116">設置</span><span class="sxs-lookup"><span data-stu-id="de306-116">Format</span></span>

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

### <span data-ttu-id="de306-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="de306-117">-Name</span></span>
<span data-ttu-id="de306-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="de306-118">WebApp Name</span></span>

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

### <span data-ttu-id="de306-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="de306-119">-OutputFile</span></span>
<span data-ttu-id="de306-120">輸出檔案</span><span class="sxs-lookup"><span data-stu-id="de306-120">Output File</span></span>

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

### <span data-ttu-id="de306-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de306-121">-ResourceGroupName</span></span>
<span data-ttu-id="de306-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="de306-122">Resource Group Name</span></span>

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

### <span data-ttu-id="de306-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="de306-123">-WebApp</span></span>
<span data-ttu-id="de306-124">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="de306-124">WebApp Object</span></span>

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

### <span data-ttu-id="de306-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de306-125">CommonParameters</span></span>
<span data-ttu-id="de306-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de306-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de306-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de306-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de306-128">輸入</span><span class="sxs-lookup"><span data-stu-id="de306-128">INPUTS</span></span>

### <span data-ttu-id="de306-129">網站地圖</span><span class="sxs-lookup"><span data-stu-id="de306-129">Site</span></span>
<span data-ttu-id="de306-130">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="de306-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="de306-131">輸出</span><span class="sxs-lookup"><span data-stu-id="de306-131">OUTPUTS</span></span>

## <span data-ttu-id="de306-132">筆記</span><span class="sxs-lookup"><span data-stu-id="de306-132">NOTES</span></span>

## <span data-ttu-id="de306-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="de306-133">RELATED LINKS</span></span>

[<span data-ttu-id="de306-134">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="de306-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="de306-135">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="de306-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


