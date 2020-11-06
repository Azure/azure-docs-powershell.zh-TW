---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: d8ccd8f1011a73068c24323bb86e39340dfc9573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448810"
---
# <span data-ttu-id="2a5f0-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="2a5f0-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="2a5f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5f0-103">取得 Azure Web App 槽發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a5f0-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a5f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a5f0-104">SYNTAX</span></span>

### <span data-ttu-id="2a5f0-105">S1</span><span class="sxs-lookup"><span data-stu-id="2a5f0-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a5f0-106">S2</span><span class="sxs-lookup"><span data-stu-id="2a5f0-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a5f0-107">說明</span><span class="sxs-lookup"><span data-stu-id="2a5f0-107">DESCRIPTION</span></span>
<span data-ttu-id="2a5f0-108">**AzureRmWebAppSlotPublishingProfile** Cmdlet 會取得指定槽的 Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a5f0-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="2a5f0-109">示例</span><span class="sxs-lookup"><span data-stu-id="2a5f0-109">EXAMPLES</span></span>

### <span data-ttu-id="2a5f0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2a5f0-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="2a5f0-111">這個命令會針對與資源群組預設的 web App ContosoWebApp 相關聯的 Slot001，以 Ftp 格式取得 Ftp 格式的發佈設定檔，並將它儲存在指定的輸出檔案中。</span><span class="sxs-lookup"><span data-stu-id="2a5f0-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="2a5f0-112">參數</span><span class="sxs-lookup"><span data-stu-id="2a5f0-112">PARAMETERS</span></span>

### <span data-ttu-id="2a5f0-113">-Format</span><span class="sxs-lookup"><span data-stu-id="2a5f0-113">-Format</span></span>
<span data-ttu-id="2a5f0-114">設置</span><span class="sxs-lookup"><span data-stu-id="2a5f0-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a5f0-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a5f0-115">-Name</span></span>
<span data-ttu-id="2a5f0-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="2a5f0-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5f0-117">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="2a5f0-117">-OutputFile</span></span>
<span data-ttu-id="2a5f0-118">輸出檔案</span><span class="sxs-lookup"><span data-stu-id="2a5f0-118">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a5f0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a5f0-119">-ResourceGroupName</span></span>
<span data-ttu-id="2a5f0-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2a5f0-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a5f0-121">-槽</span><span class="sxs-lookup"><span data-stu-id="2a5f0-121">-Slot</span></span>
<span data-ttu-id="2a5f0-122">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="2a5f0-122">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a5f0-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2a5f0-123">-WebApp</span></span>
<span data-ttu-id="2a5f0-124">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="2a5f0-124">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5f0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a5f0-125">-DefaultProfile</span></span>
<span data-ttu-id="2a5f0-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a5f0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a5f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5f0-127">CommonParameters</span></span>
<span data-ttu-id="2a5f0-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a5f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5f0-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a5f0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5f0-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2a5f0-130">INPUTS</span></span>

### <span data-ttu-id="2a5f0-131">網站地圖</span><span class="sxs-lookup"><span data-stu-id="2a5f0-131">Site</span></span>
<span data-ttu-id="2a5f0-132">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2a5f0-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2a5f0-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2a5f0-133">OUTPUTS</span></span>

## <span data-ttu-id="2a5f0-134">筆記</span><span class="sxs-lookup"><span data-stu-id="2a5f0-134">NOTES</span></span>

## <span data-ttu-id="2a5f0-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a5f0-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a5f0-136">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="2a5f0-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="2a5f0-137">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2a5f0-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="2a5f0-138">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2a5f0-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
