---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: a2c57ebe6f85209596628dffe9de88ca260bbafa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958541"
---
# <span data-ttu-id="fae10-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="fae10-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="fae10-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fae10-102">SYNOPSIS</span></span>
<span data-ttu-id="fae10-103">設定 Web 應用程式槽配置名稱</span><span class="sxs-lookup"><span data-stu-id="fae10-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="fae10-104">句法</span><span class="sxs-lookup"><span data-stu-id="fae10-104">SYNTAX</span></span>

### <span data-ttu-id="fae10-105">S1</span><span class="sxs-lookup"><span data-stu-id="fae10-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fae10-106">S2</span><span class="sxs-lookup"><span data-stu-id="fae10-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fae10-107">說明</span><span class="sxs-lookup"><span data-stu-id="fae10-107">DESCRIPTION</span></span>
<span data-ttu-id="fae10-108">**AzWebAppSlotConfigName** Cmdlet 會將 App 設定和連接字串標示為槽設定</span><span class="sxs-lookup"><span data-stu-id="fae10-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="fae10-109">示例</span><span class="sxs-lookup"><span data-stu-id="fae10-109">EXAMPLES</span></span>

### <span data-ttu-id="fae10-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="fae10-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="fae10-111">這個命令會移除與資源群組預設-Web-WestUS 相關聯之 Web App ContosoWebApp 的所有 app 設定和連線字串。</span><span class="sxs-lookup"><span data-stu-id="fae10-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="fae10-112">參數</span><span class="sxs-lookup"><span data-stu-id="fae10-112">PARAMETERS</span></span>

### <span data-ttu-id="fae10-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="fae10-113">-AppSettingNames</span></span>
<span data-ttu-id="fae10-114">應用程式設定名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="fae10-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="fae10-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="fae10-115">-ConnectionStringNames</span></span>
<span data-ttu-id="fae10-116">連接字串名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="fae10-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="fae10-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae10-117">-DefaultProfile</span></span>
<span data-ttu-id="fae10-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fae10-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae10-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fae10-119">-Name</span></span>
<span data-ttu-id="fae10-120">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="fae10-120">WebApp Name</span></span>

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

### <span data-ttu-id="fae10-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="fae10-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="fae10-122">[移除所有 App 設定名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="fae10-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="fae10-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="fae10-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="fae10-124">[移除所有連線字串名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="fae10-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="fae10-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae10-125">-ResourceGroupName</span></span>
<span data-ttu-id="fae10-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="fae10-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fae10-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fae10-127">-WebApp</span></span>
<span data-ttu-id="fae10-128">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="fae10-128">WebApp Object</span></span>

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

### <span data-ttu-id="fae10-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae10-129">CommonParameters</span></span>
<span data-ttu-id="fae10-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fae10-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae10-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fae10-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae10-132">輸入</span><span class="sxs-lookup"><span data-stu-id="fae10-132">INPUTS</span></span>

### <span data-ttu-id="fae10-133">System.object []</span><span class="sxs-lookup"><span data-stu-id="fae10-133">System.String[]</span></span>

### <span data-ttu-id="fae10-134">System.object</span><span class="sxs-lookup"><span data-stu-id="fae10-134">System.String</span></span>

### <span data-ttu-id="fae10-135">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="fae10-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fae10-136">輸出</span><span class="sxs-lookup"><span data-stu-id="fae10-136">OUTPUTS</span></span>

### <span data-ttu-id="fae10-137">SlotConfigNamesResource 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="fae10-137">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="fae10-138">筆記</span><span class="sxs-lookup"><span data-stu-id="fae10-138">NOTES</span></span>

## <span data-ttu-id="fae10-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="fae10-139">RELATED LINKS</span></span>
