---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140694"
---
# <span data-ttu-id="e22b4-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e22b4-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="e22b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e22b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e22b4-103">從槽中移除路由規則。</span><span class="sxs-lookup"><span data-stu-id="e22b4-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="e22b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="e22b4-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e22b4-105">說明</span><span class="sxs-lookup"><span data-stu-id="e22b4-105">DESCRIPTION</span></span>
<span data-ttu-id="e22b4-106">**AzWebAppTrafficRouting** Cmdlet 會從 Azure Web App 槽中移除路由規則。</span><span class="sxs-lookup"><span data-stu-id="e22b4-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="e22b4-107">示例</span><span class="sxs-lookup"><span data-stu-id="e22b4-107">EXAMPLES</span></span>

### <span data-ttu-id="e22b4-108">範例1從 webapp 槽中移除特定的路由規則</span><span class="sxs-lookup"><span data-stu-id="e22b4-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="e22b4-109">這個命令會移除指定 webapp 槽的路由規則。</span><span class="sxs-lookup"><span data-stu-id="e22b4-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="e22b4-110">參數</span><span class="sxs-lookup"><span data-stu-id="e22b4-110">PARAMETERS</span></span>

### <span data-ttu-id="e22b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22b4-111">-DefaultProfile</span></span>
<span data-ttu-id="e22b4-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e22b4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e22b4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e22b4-113">-ResourceGroupName</span></span>
<span data-ttu-id="e22b4-114">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e22b4-114">Resource Group Name</span></span>

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

### <span data-ttu-id="e22b4-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="e22b4-115">-RuleName</span></span>
<span data-ttu-id="e22b4-116">規則名稱</span><span class="sxs-lookup"><span data-stu-id="e22b4-116">Rule Name</span></span>

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

### <span data-ttu-id="e22b4-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="e22b4-117">-WebAppName</span></span>
<span data-ttu-id="e22b4-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="e22b4-118">WebApp Name</span></span>

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

### <span data-ttu-id="e22b4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e22b4-119">-PassThru</span></span>
<span data-ttu-id="e22b4-120">傳回 [存取限制] 設定物件。</span><span class="sxs-lookup"><span data-stu-id="e22b4-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="e22b4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="e22b4-121">-Confirm</span></span>
<span data-ttu-id="e22b4-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e22b4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e22b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e22b4-123">-WhatIf</span></span>
<span data-ttu-id="e22b4-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e22b4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e22b4-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e22b4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e22b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22b4-126">CommonParameters</span></span>
<span data-ttu-id="e22b4-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e22b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22b4-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e22b4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22b4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e22b4-129">INPUTS</span></span>

### <span data-ttu-id="e22b4-130">所有</span><span class="sxs-lookup"><span data-stu-id="e22b4-130">None</span></span>

## <span data-ttu-id="e22b4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e22b4-131">OUTPUTS</span></span>

### <span data-ttu-id="e22b4-132">RampUpRule 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="e22b4-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="e22b4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e22b4-133">NOTES</span></span>

## <span data-ttu-id="e22b4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e22b4-134">RELATED LINKS</span></span>
[<span data-ttu-id="e22b4-135">附加 AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e22b4-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="e22b4-136">AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e22b4-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="e22b4-137">更新-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e22b4-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)