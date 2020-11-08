---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137086"
---
# <span data-ttu-id="41376-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="41376-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="41376-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41376-102">SYNOPSIS</span></span>
<span data-ttu-id="41376-103">移除裝置上的使用者。</span><span class="sxs-lookup"><span data-stu-id="41376-103">Removes a user on a device.</span></span>

## <span data-ttu-id="41376-104">句法</span><span class="sxs-lookup"><span data-stu-id="41376-104">SYNTAX</span></span>

### <span data-ttu-id="41376-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="41376-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41376-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41376-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41376-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41376-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41376-108">說明</span><span class="sxs-lookup"><span data-stu-id="41376-108">DESCRIPTION</span></span>
<span data-ttu-id="41376-109">**AzStackEdgeUser** Cmdlet 會移除堆疊 Edge 裝置上的使用者。</span><span class="sxs-lookup"><span data-stu-id="41376-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="41376-110">只支援建立 type 類型的使用者 `Share` 。</span><span class="sxs-lookup"><span data-stu-id="41376-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="41376-111">示例</span><span class="sxs-lookup"><span data-stu-id="41376-111">EXAMPLES</span></span>

### <span data-ttu-id="41376-112">範例1</span><span class="sxs-lookup"><span data-stu-id="41376-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="41376-113">參數</span><span class="sxs-lookup"><span data-stu-id="41376-113">PARAMETERS</span></span>

### <span data-ttu-id="41376-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41376-114">-AsJob</span></span>
<span data-ttu-id="41376-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41376-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41376-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41376-116">-DefaultProfile</span></span>
<span data-ttu-id="41376-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41376-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41376-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="41376-118">-DeviceName</span></span>
<span data-ttu-id="41376-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="41376-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41376-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41376-120">-InputObject</span></span>
<span data-ttu-id="41376-121">輸入物件</span><span class="sxs-lookup"><span data-stu-id="41376-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41376-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="41376-122">-Name</span></span>
<span data-ttu-id="41376-123">Username</span><span class="sxs-lookup"><span data-stu-id="41376-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41376-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41376-124">-PassThru</span></span>
<span data-ttu-id="41376-125">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="41376-125">returns true if successful</span></span>

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

### <span data-ttu-id="41376-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41376-126">-ResourceGroupName</span></span>
<span data-ttu-id="41376-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="41376-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41376-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41376-128">-ResourceId</span></span>
<span data-ttu-id="41376-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="41376-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41376-130">-確認</span><span class="sxs-lookup"><span data-stu-id="41376-130">-Confirm</span></span>
<span data-ttu-id="41376-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41376-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41376-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41376-132">-WhatIf</span></span>
<span data-ttu-id="41376-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41376-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41376-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41376-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41376-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41376-135">CommonParameters</span></span>
<span data-ttu-id="41376-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41376-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41376-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="41376-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41376-138">輸入</span><span class="sxs-lookup"><span data-stu-id="41376-138">INPUTS</span></span>

### <span data-ttu-id="41376-139">System.object</span><span class="sxs-lookup"><span data-stu-id="41376-139">System.String</span></span>

### <span data-ttu-id="41376-140">PSStackEdgeUser （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="41376-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="41376-141">輸出</span><span class="sxs-lookup"><span data-stu-id="41376-141">OUTPUTS</span></span>

### <span data-ttu-id="41376-142">PSStackEdgeStorageAccountCredential （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="41376-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="41376-143">筆記</span><span class="sxs-lookup"><span data-stu-id="41376-143">NOTES</span></span>

## <span data-ttu-id="41376-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="41376-144">RELATED LINKS</span></span>