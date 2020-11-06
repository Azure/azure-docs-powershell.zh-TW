---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 75c134b162636f94b00cf6692f4e9df120930dcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449648"
---
# <span data-ttu-id="c35f9-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="c35f9-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="c35f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c35f9-102">SYNOPSIS</span></span>
<span data-ttu-id="c35f9-103">設定 Web 應用程式槽配置名稱</span><span class="sxs-lookup"><span data-stu-id="c35f9-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c35f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c35f9-104">SYNTAX</span></span>

### <span data-ttu-id="c35f9-105">S1</span><span class="sxs-lookup"><span data-stu-id="c35f9-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c35f9-106">S2</span><span class="sxs-lookup"><span data-stu-id="c35f9-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c35f9-107">說明</span><span class="sxs-lookup"><span data-stu-id="c35f9-107">DESCRIPTION</span></span>
<span data-ttu-id="c35f9-108">**AzureRmWebAppSlotConfigName** Cmdlet 會將 App 設定和連接字串標示為槽設定</span><span class="sxs-lookup"><span data-stu-id="c35f9-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="c35f9-109">示例</span><span class="sxs-lookup"><span data-stu-id="c35f9-109">EXAMPLES</span></span>

### <span data-ttu-id="c35f9-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="c35f9-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="c35f9-111">這個命令會移除與資源群組預設-Web-WestUS 相關聯之 Web App ContosoWebApp 的所有 app 設定和連線字串。</span><span class="sxs-lookup"><span data-stu-id="c35f9-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c35f9-112">參數</span><span class="sxs-lookup"><span data-stu-id="c35f9-112">PARAMETERS</span></span>

### <span data-ttu-id="c35f9-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="c35f9-113">-AppSettingNames</span></span>
<span data-ttu-id="c35f9-114">應用程式設定名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="c35f9-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c35f9-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="c35f9-115">-ConnectionStringNames</span></span>
<span data-ttu-id="c35f9-116">連接字串名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="c35f9-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c35f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c35f9-117">-DefaultProfile</span></span>
<span data-ttu-id="c35f9-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c35f9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c35f9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c35f9-119">-Name</span></span>
<span data-ttu-id="c35f9-120">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="c35f9-120">WebApp Name</span></span>

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

### <span data-ttu-id="c35f9-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="c35f9-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="c35f9-122">[移除所有 App 設定名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="c35f9-122">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35f9-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="c35f9-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="c35f9-124">[移除所有連線字串名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="c35f9-124">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c35f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="c35f9-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c35f9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c35f9-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c35f9-127">-WebApp</span></span>
<span data-ttu-id="c35f9-128">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="c35f9-128">WebApp Object</span></span>

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

### <span data-ttu-id="c35f9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c35f9-129">CommonParameters</span></span>
<span data-ttu-id="c35f9-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c35f9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c35f9-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c35f9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c35f9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c35f9-132">INPUTS</span></span>

### <span data-ttu-id="c35f9-133">System.object []</span><span class="sxs-lookup"><span data-stu-id="c35f9-133">System.String[]</span></span>

### <span data-ttu-id="c35f9-134">System.object</span><span class="sxs-lookup"><span data-stu-id="c35f9-134">System.String</span></span>

### <span data-ttu-id="c35f9-135">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="c35f9-135">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c35f9-136">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c35f9-136">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="c35f9-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c35f9-137">OUTPUTS</span></span>

### <span data-ttu-id="c35f9-138">SlotConfigNamesResource 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="c35f9-138">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="c35f9-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c35f9-139">NOTES</span></span>

## <span data-ttu-id="c35f9-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c35f9-140">RELATED LINKS</span></span>
