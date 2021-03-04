---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: 8ef763300d530c764aefc3fa18c6bbf2a781b4b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905846"
---
# <span data-ttu-id="ff42a-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ff42a-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="ff42a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ff42a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff42a-103">移除管理群組</span><span class="sxs-lookup"><span data-stu-id="ff42a-103">Removes a Management Group</span></span>

## <span data-ttu-id="ff42a-104">語法</span><span class="sxs-lookup"><span data-stu-id="ff42a-104">SYNTAX</span></span>

### <span data-ttu-id="ff42a-105">GroupOperations (預設) </span><span class="sxs-lookup"><span data-stu-id="ff42a-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff42a-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="ff42a-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff42a-107">描述</span><span class="sxs-lookup"><span data-stu-id="ff42a-107">DESCRIPTION</span></span>
<span data-ttu-id="ff42a-108">**Remove-AzManagementGroup** Cmdlet 會刪除管理群組。</span><span class="sxs-lookup"><span data-stu-id="ff42a-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="ff42a-109">例子</span><span class="sxs-lookup"><span data-stu-id="ff42a-109">EXAMPLES</span></span>

### <span data-ttu-id="ff42a-110">範例 1：移除管理群組</span><span class="sxs-lookup"><span data-stu-id="ff42a-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="ff42a-111">範例 2：使用 PSManagementGroup 物件管道移除管理群組</span><span class="sxs-lookup"><span data-stu-id="ff42a-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="ff42a-112">參數</span><span class="sxs-lookup"><span data-stu-id="ff42a-112">PARAMETERS</span></span>

### <span data-ttu-id="ff42a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff42a-113">-DefaultProfile</span></span>
<span data-ttu-id="ff42a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff42a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff42a-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="ff42a-115">-GroupName</span></span>
<span data-ttu-id="ff42a-116">管理群組識別碼</span><span class="sxs-lookup"><span data-stu-id="ff42a-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff42a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff42a-117">-InputObject</span></span>
<span data-ttu-id="ff42a-118">從 Get 通話輸入物件</span><span class="sxs-lookup"><span data-stu-id="ff42a-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff42a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff42a-119">-PassThru</span></span>
<span data-ttu-id="ff42a-120">成功 `true` 執行時返回</span><span class="sxs-lookup"><span data-stu-id="ff42a-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="ff42a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ff42a-121">-Confirm</span></span>
<span data-ttu-id="ff42a-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ff42a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff42a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff42a-123">-WhatIf</span></span>
<span data-ttu-id="ff42a-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff42a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff42a-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff42a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff42a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff42a-126">CommonParameters</span></span>
<span data-ttu-id="ff42a-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ff42a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff42a-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff42a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff42a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ff42a-129">INPUTS</span></span>

### <span data-ttu-id="ff42a-130">Microsoft.Azure.Commands.Resources.models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ff42a-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="ff42a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ff42a-131">OUTPUTS</span></span>

### <span data-ttu-id="ff42a-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff42a-132">System.Boolean</span></span>

## <span data-ttu-id="ff42a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ff42a-133">NOTES</span></span>

## <span data-ttu-id="ff42a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff42a-134">RELATED LINKS</span></span>
