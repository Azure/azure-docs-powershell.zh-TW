---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: b58ffa98f3f35a8e8f87785e4d7abb703aa9b90e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908089"
---
# <span data-ttu-id="5367d-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="5367d-101">Remove-AzBastion</span></span>

## <span data-ttu-id="5367d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5367d-102">SYNOPSIS</span></span>
<span data-ttu-id="5367d-103">移除基礎資源。</span><span class="sxs-lookup"><span data-stu-id="5367d-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="5367d-104">語法</span><span class="sxs-lookup"><span data-stu-id="5367d-104">SYNTAX</span></span>

### <span data-ttu-id="5367d-105">ByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="5367d-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5367d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5367d-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5367d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5367d-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5367d-108">描述</span><span class="sxs-lookup"><span data-stu-id="5367d-108">DESCRIPTION</span></span>
<span data-ttu-id="5367d-109">移除基礎資源。範例1 會使用其 ResourceGroupName 和 ResourceName 刪除 bastion。</span><span class="sxs-lookup"><span data-stu-id="5367d-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="5367d-110">範例 2 會使用物件與管線一起刪除 bastion。</span><span class="sxs-lookup"><span data-stu-id="5367d-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="5367d-111">Example3 會使用其物件刪除 bastion。</span><span class="sxs-lookup"><span data-stu-id="5367d-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="5367d-112">例子</span><span class="sxs-lookup"><span data-stu-id="5367d-112">EXAMPLES</span></span>

### <span data-ttu-id="5367d-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="5367d-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="5367d-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="5367d-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="5367d-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="5367d-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="5367d-116">參數</span><span class="sxs-lookup"><span data-stu-id="5367d-116">PARAMETERS</span></span>

### <span data-ttu-id="5367d-117">-確認</span><span class="sxs-lookup"><span data-stu-id="5367d-117">-Confirm</span></span>
<span data-ttu-id="5367d-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5367d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5367d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5367d-119">-DefaultProfile</span></span>
<span data-ttu-id="5367d-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5367d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5367d-121">-強制</span><span class="sxs-lookup"><span data-stu-id="5367d-121">-Force</span></span>
<span data-ttu-id="5367d-122">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="5367d-122">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5367d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5367d-123">-InputObject</span></span>
<span data-ttu-id="5367d-124">要刪除的 Bastion 物件。</span><span class="sxs-lookup"><span data-stu-id="5367d-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5367d-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="5367d-125">-Name</span></span>
<span data-ttu-id="5367d-126">要刪除的基地資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5367d-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5367d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5367d-127">-PassThru</span></span>
<span data-ttu-id="5367d-128">會返回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="5367d-128">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5367d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5367d-129">-ResourceGroupName</span></span>
<span data-ttu-id="5367d-130">存在 bastion 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="5367d-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5367d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5367d-131">-ResourceId</span></span>
<span data-ttu-id="5367d-132">要刪除的 Bastion Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5367d-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5367d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5367d-133">-WhatIf</span></span>
<span data-ttu-id="5367d-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5367d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5367d-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5367d-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5367d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5367d-136">CommonParameters</span></span>
<span data-ttu-id="5367d-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5367d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5367d-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5367d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5367d-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5367d-139">INPUTS</span></span>

### <span data-ttu-id="5367d-140">Microsoft.Azure.Commands.Network.models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="5367d-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="5367d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5367d-141">System.String</span></span>

## <span data-ttu-id="5367d-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5367d-142">OUTPUTS</span></span>

### <span data-ttu-id="5367d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5367d-143">System.Boolean</span></span>

## <span data-ttu-id="5367d-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5367d-144">NOTES</span></span>

## <span data-ttu-id="5367d-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5367d-145">RELATED LINKS</span></span>
[<span data-ttu-id="5367d-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="5367d-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="5367d-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="5367d-147">New-AzBastion</span></span>](./New-AzBastion.md)