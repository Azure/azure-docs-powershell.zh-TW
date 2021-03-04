---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911822"
---
# <span data-ttu-id="75f56-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="75f56-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="75f56-102">簡介</span><span class="sxs-lookup"><span data-stu-id="75f56-102">SYNOPSIS</span></span>
<span data-ttu-id="75f56-103">從 Slot 移除路由規則。</span><span class="sxs-lookup"><span data-stu-id="75f56-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="75f56-104">語法</span><span class="sxs-lookup"><span data-stu-id="75f56-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75f56-105">描述</span><span class="sxs-lookup"><span data-stu-id="75f56-105">DESCRIPTION</span></span>
<span data-ttu-id="75f56-106">**Remove-AzWebAppTrafficRoudlet** 會從 Azure Web App Slot 移除路由規則。</span><span class="sxs-lookup"><span data-stu-id="75f56-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="75f56-107">例子</span><span class="sxs-lookup"><span data-stu-id="75f56-107">EXAMPLES</span></span>

### <span data-ttu-id="75f56-108">範例 1 移除 Webapp 插槽中的特定路由規則</span><span class="sxs-lookup"><span data-stu-id="75f56-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="75f56-109">此命令會移除給定 Webapp 插槽的路由規則。</span><span class="sxs-lookup"><span data-stu-id="75f56-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="75f56-110">參數</span><span class="sxs-lookup"><span data-stu-id="75f56-110">PARAMETERS</span></span>

### <span data-ttu-id="75f56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f56-111">-DefaultProfile</span></span>
<span data-ttu-id="75f56-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="75f56-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75f56-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f56-113">-ResourceGroupName</span></span>
<span data-ttu-id="75f56-114">資源組名</span><span class="sxs-lookup"><span data-stu-id="75f56-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f56-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="75f56-115">-RuleName</span></span>
<span data-ttu-id="75f56-116">規則名稱</span><span class="sxs-lookup"><span data-stu-id="75f56-116">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f56-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="75f56-117">-WebAppName</span></span>
<span data-ttu-id="75f56-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="75f56-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f56-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75f56-119">-PassThru</span></span>
<span data-ttu-id="75f56-120">返回存取限制設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="75f56-120">Return the access restriction config object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f56-121">-確認</span><span class="sxs-lookup"><span data-stu-id="75f56-121">-Confirm</span></span>
<span data-ttu-id="75f56-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="75f56-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f56-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75f56-123">-WhatIf</span></span>
<span data-ttu-id="75f56-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="75f56-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75f56-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75f56-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f56-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f56-126">CommonParameters</span></span>
<span data-ttu-id="75f56-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="75f56-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f56-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75f56-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f56-129">輸入</span><span class="sxs-lookup"><span data-stu-id="75f56-129">INPUTS</span></span>

### <span data-ttu-id="75f56-130">沒有</span><span class="sxs-lookup"><span data-stu-id="75f56-130">None</span></span>

## <span data-ttu-id="75f56-131">輸出</span><span class="sxs-lookup"><span data-stu-id="75f56-131">OUTPUTS</span></span>

### <span data-ttu-id="75f56-132">Microsoft.Azure.management.Websites.models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="75f56-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="75f56-133">筆記</span><span class="sxs-lookup"><span data-stu-id="75f56-133">NOTES</span></span>

## <span data-ttu-id="75f56-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="75f56-134">RELATED LINKS</span></span>
[<span data-ttu-id="75f56-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="75f56-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="75f56-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="75f56-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="75f56-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="75f56-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)