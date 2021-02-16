---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ce2ccd21d7adecdf9602d29837295ad2ca65c952
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139951"
---
# <span data-ttu-id="20f51-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="20f51-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="20f51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20f51-102">SYNOPSIS</span></span>
<span data-ttu-id="20f51-103">移除管理群組</span><span class="sxs-lookup"><span data-stu-id="20f51-103">Removes a Management Group</span></span>

## <span data-ttu-id="20f51-104">句法</span><span class="sxs-lookup"><span data-stu-id="20f51-104">SYNTAX</span></span>

### <span data-ttu-id="20f51-105">GroupOperations (預設) </span><span class="sxs-lookup"><span data-stu-id="20f51-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20f51-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="20f51-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20f51-107">說明</span><span class="sxs-lookup"><span data-stu-id="20f51-107">DESCRIPTION</span></span>
<span data-ttu-id="20f51-108">**AzManagementGroup** Cmdlet 會刪除管理群組。</span><span class="sxs-lookup"><span data-stu-id="20f51-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="20f51-109">示例</span><span class="sxs-lookup"><span data-stu-id="20f51-109">EXAMPLES</span></span>

### <span data-ttu-id="20f51-110">範例1：移除管理群組</span><span class="sxs-lookup"><span data-stu-id="20f51-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="20f51-111">範例2：依管道 PSManagementGroup 物件移除管理群組</span><span class="sxs-lookup"><span data-stu-id="20f51-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="20f51-112">參數</span><span class="sxs-lookup"><span data-stu-id="20f51-112">PARAMETERS</span></span>

### <span data-ttu-id="20f51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f51-113">-DefaultProfile</span></span>
<span data-ttu-id="20f51-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20f51-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20f51-115">-[名]</span><span class="sxs-lookup"><span data-stu-id="20f51-115">-GroupName</span></span>
<span data-ttu-id="20f51-116">管理群組識別碼</span><span class="sxs-lookup"><span data-stu-id="20f51-116">Management Group Id</span></span>

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

### <span data-ttu-id="20f51-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20f51-117">-InputObject</span></span>
<span data-ttu-id="20f51-118">從 [取得通話] 輸入物件</span><span class="sxs-lookup"><span data-stu-id="20f51-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="20f51-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20f51-119">-PassThru</span></span>
<span data-ttu-id="20f51-120">`true`成功執行後返回</span><span class="sxs-lookup"><span data-stu-id="20f51-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="20f51-121">-確認</span><span class="sxs-lookup"><span data-stu-id="20f51-121">-Confirm</span></span>
<span data-ttu-id="20f51-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="20f51-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f51-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f51-123">-WhatIf</span></span>
<span data-ttu-id="20f51-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20f51-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20f51-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20f51-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f51-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f51-126">CommonParameters</span></span>
<span data-ttu-id="20f51-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20f51-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f51-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="20f51-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f51-129">輸入</span><span class="sxs-lookup"><span data-stu-id="20f51-129">INPUTS</span></span>

### <span data-ttu-id="20f51-130">[ManagementGroups].. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="20f51-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="20f51-131">輸出</span><span class="sxs-lookup"><span data-stu-id="20f51-131">OUTPUTS</span></span>

### <span data-ttu-id="20f51-132">System.object</span><span class="sxs-lookup"><span data-stu-id="20f51-132">System.Boolean</span></span>

## <span data-ttu-id="20f51-133">筆記</span><span class="sxs-lookup"><span data-stu-id="20f51-133">NOTES</span></span>

## <span data-ttu-id="20f51-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="20f51-134">RELATED LINKS</span></span>
