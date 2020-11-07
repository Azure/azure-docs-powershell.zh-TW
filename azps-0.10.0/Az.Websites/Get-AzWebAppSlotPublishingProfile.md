---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: cedaf16333d69a25dce0ce2657640e723767aece
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794981"
---
# <span data-ttu-id="e0781-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e0781-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="e0781-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0781-102">SYNOPSIS</span></span>
<span data-ttu-id="e0781-103">取得 Azure Web App 槽發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="e0781-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="e0781-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0781-104">SYNTAX</span></span>

### <span data-ttu-id="e0781-105">S1</span><span class="sxs-lookup"><span data-stu-id="e0781-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0781-106">S2</span><span class="sxs-lookup"><span data-stu-id="e0781-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0781-107">說明</span><span class="sxs-lookup"><span data-stu-id="e0781-107">DESCRIPTION</span></span>
<span data-ttu-id="e0781-108">**AzWebAppSlotPublishingProfile** Cmdlet 會取得指定槽的 Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="e0781-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="e0781-109">示例</span><span class="sxs-lookup"><span data-stu-id="e0781-109">EXAMPLES</span></span>

### <span data-ttu-id="e0781-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e0781-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="e0781-111">這個命令會針對與資源群組預設的 web App ContosoWebApp 相關聯的 Slot001，以 Ftp 格式取得 Ftp 格式的發佈設定檔，並將它儲存在指定的輸出檔案中。</span><span class="sxs-lookup"><span data-stu-id="e0781-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="e0781-112">參數</span><span class="sxs-lookup"><span data-stu-id="e0781-112">PARAMETERS</span></span>

### <span data-ttu-id="e0781-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0781-113">-DefaultProfile</span></span>
<span data-ttu-id="e0781-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0781-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0781-115">-Format</span><span class="sxs-lookup"><span data-stu-id="e0781-115">-Format</span></span>
<span data-ttu-id="e0781-116">設置</span><span class="sxs-lookup"><span data-stu-id="e0781-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0781-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0781-117">-Name</span></span>
<span data-ttu-id="e0781-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="e0781-118">WebApp Name</span></span>

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

### <span data-ttu-id="e0781-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="e0781-119">-OutputFile</span></span>
<span data-ttu-id="e0781-120">輸出檔案</span><span class="sxs-lookup"><span data-stu-id="e0781-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0781-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0781-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0781-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e0781-122">Resource Group Name</span></span>

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

### <span data-ttu-id="e0781-123">-槽</span><span class="sxs-lookup"><span data-stu-id="e0781-123">-Slot</span></span>
<span data-ttu-id="e0781-124">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="e0781-124">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0781-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e0781-125">-WebApp</span></span>
<span data-ttu-id="e0781-126">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="e0781-126">WebApp Object</span></span>

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

### <span data-ttu-id="e0781-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0781-127">CommonParameters</span></span>
<span data-ttu-id="e0781-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0781-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0781-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0781-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0781-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e0781-130">INPUTS</span></span>

### <span data-ttu-id="e0781-131">網站地圖</span><span class="sxs-lookup"><span data-stu-id="e0781-131">Site</span></span>
<span data-ttu-id="e0781-132">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e0781-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e0781-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e0781-133">OUTPUTS</span></span>

## <span data-ttu-id="e0781-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e0781-134">NOTES</span></span>

## <span data-ttu-id="e0781-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0781-135">RELATED LINKS</span></span>

[<span data-ttu-id="e0781-136">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e0781-136">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="e0781-137">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e0781-137">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="e0781-138">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e0781-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
