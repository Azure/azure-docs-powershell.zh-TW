---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 29ef83bf3ed0f423686e7ddf84bc82555bd09572
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443631"
---
# <span data-ttu-id="3df44-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="3df44-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="3df44-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3df44-102">SYNOPSIS</span></span>
<span data-ttu-id="3df44-103">取得 Azure Web App 槽發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="3df44-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3df44-104">句法</span><span class="sxs-lookup"><span data-stu-id="3df44-104">SYNTAX</span></span>

### <span data-ttu-id="3df44-105">S1</span><span class="sxs-lookup"><span data-stu-id="3df44-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3df44-106">S2</span><span class="sxs-lookup"><span data-stu-id="3df44-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3df44-107">說明</span><span class="sxs-lookup"><span data-stu-id="3df44-107">DESCRIPTION</span></span>
<span data-ttu-id="3df44-108">**AzureRmWebAppSlotPublishingProfile** Cmdlet 會取得指定槽的 Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="3df44-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="3df44-109">示例</span><span class="sxs-lookup"><span data-stu-id="3df44-109">EXAMPLES</span></span>

### <span data-ttu-id="3df44-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3df44-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="3df44-111">這個命令會針對與資源群組預設的 web App ContosoWebApp 相關聯的 Slot001，以 Ftp 格式取得 Ftp 格式的發佈設定檔，並將它儲存在指定的輸出檔案中。</span><span class="sxs-lookup"><span data-stu-id="3df44-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="3df44-112">參數</span><span class="sxs-lookup"><span data-stu-id="3df44-112">PARAMETERS</span></span>

### <span data-ttu-id="3df44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df44-113">-DefaultProfile</span></span>
<span data-ttu-id="3df44-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3df44-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3df44-115">-Format</span><span class="sxs-lookup"><span data-stu-id="3df44-115">-Format</span></span>
<span data-ttu-id="3df44-116">設置</span><span class="sxs-lookup"><span data-stu-id="3df44-116">Format</span></span>

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

### <span data-ttu-id="3df44-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="3df44-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="3df44-118">如果 true，則包含災害復原端點</span><span class="sxs-lookup"><span data-stu-id="3df44-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df44-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3df44-119">-Name</span></span>
<span data-ttu-id="3df44-120">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="3df44-120">WebApp Name</span></span>

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

### <span data-ttu-id="3df44-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="3df44-121">-OutputFile</span></span>
<span data-ttu-id="3df44-122">輸出檔案</span><span class="sxs-lookup"><span data-stu-id="3df44-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df44-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df44-123">-ResourceGroupName</span></span>
<span data-ttu-id="3df44-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3df44-124">Resource Group Name</span></span>

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

### <span data-ttu-id="3df44-125">-槽</span><span class="sxs-lookup"><span data-stu-id="3df44-125">-Slot</span></span>
<span data-ttu-id="3df44-126">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="3df44-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="3df44-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3df44-127">-WebApp</span></span>
<span data-ttu-id="3df44-128">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="3df44-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3df44-129">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="3df44-129">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="3df44-130">如果 true，則包含災害復原端點</span><span class="sxs-lookup"><span data-stu-id="3df44-130">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df44-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df44-131">CommonParameters</span></span>
<span data-ttu-id="3df44-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3df44-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df44-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3df44-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df44-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3df44-134">INPUTS</span></span>

### <span data-ttu-id="3df44-135">System.object</span><span class="sxs-lookup"><span data-stu-id="3df44-135">System.String</span></span>

### <span data-ttu-id="3df44-136">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="3df44-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="3df44-137">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="3df44-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="3df44-138">輸出</span><span class="sxs-lookup"><span data-stu-id="3df44-138">OUTPUTS</span></span>

### <span data-ttu-id="3df44-139">System.object</span><span class="sxs-lookup"><span data-stu-id="3df44-139">System.String</span></span>

## <span data-ttu-id="3df44-140">筆記</span><span class="sxs-lookup"><span data-stu-id="3df44-140">NOTES</span></span>

## <span data-ttu-id="3df44-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="3df44-141">RELATED LINKS</span></span>

[<span data-ttu-id="3df44-142">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="3df44-142">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="3df44-143">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3df44-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="3df44-144">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3df44-144">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
