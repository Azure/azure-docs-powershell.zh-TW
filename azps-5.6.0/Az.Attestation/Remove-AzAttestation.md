---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 564c3d9a67e3a006a7ce7871419e236a71838a42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905226"
---
# <span data-ttu-id="830b4-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="830b4-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="830b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="830b4-102">SYNOPSIS</span></span>
<span data-ttu-id="830b4-103">刪除證明。</span><span class="sxs-lookup"><span data-stu-id="830b4-103">Deletes an attestation.</span></span>

## <span data-ttu-id="830b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="830b4-104">SYNTAX</span></span>

### <span data-ttu-id="830b4-105">ByAvailableAttestation (預設) </span><span class="sxs-lookup"><span data-stu-id="830b4-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="830b4-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="830b4-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="830b4-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="830b4-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="830b4-108">描述</span><span class="sxs-lookup"><span data-stu-id="830b4-108">DESCRIPTION</span></span>
<span data-ttu-id="830b4-109">Cmdlet Remove-AzAttestation刪除指定的證明。</span><span class="sxs-lookup"><span data-stu-id="830b4-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="830b4-110">例子</span><span class="sxs-lookup"><span data-stu-id="830b4-110">EXAMPLES</span></span>

### <span data-ttu-id="830b4-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="830b4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="830b4-112">刪除目前訂閱中名為 *psh-test-rg 的資源群組中名為 psh-test-rg* 的驗證提供者。 </span><span class="sxs-lookup"><span data-stu-id="830b4-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="830b4-113">參數</span><span class="sxs-lookup"><span data-stu-id="830b4-113">PARAMETERS</span></span>

### <span data-ttu-id="830b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830b4-114">-DefaultProfile</span></span>
<span data-ttu-id="830b4-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="830b4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="830b4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="830b4-116">-InputObject</span></span>
<span data-ttu-id="830b4-117">要刪除的表示物件。</span><span class="sxs-lookup"><span data-stu-id="830b4-117">Attestation object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Attestation.Models.PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="830b4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="830b4-118">-Name</span></span>
<span data-ttu-id="830b4-119">指定要移除之證明的名稱。</span><span class="sxs-lookup"><span data-stu-id="830b4-119">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830b4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="830b4-120">-PassThru</span></span>
<span data-ttu-id="830b4-121">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="830b4-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="830b4-122">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="830b4-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="830b4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="830b4-123">-ResourceGroupName</span></span>
<span data-ttu-id="830b4-124">指定要移除的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="830b4-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830b4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="830b4-125">-ResourceId</span></span>
<span data-ttu-id="830b4-126">證明資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="830b4-126">Attestation Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830b4-127">-確認</span><span class="sxs-lookup"><span data-stu-id="830b4-127">-Confirm</span></span>
<span data-ttu-id="830b4-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="830b4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="830b4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="830b4-129">-WhatIf</span></span>
<span data-ttu-id="830b4-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="830b4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="830b4-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="830b4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="830b4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830b4-132">CommonParameters</span></span>
<span data-ttu-id="830b4-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="830b4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830b4-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="830b4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830b4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="830b4-135">INPUTS</span></span>

### <span data-ttu-id="830b4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="830b4-136">System.String</span></span>

### <span data-ttu-id="830b4-137">Microsoft.Azure.Commands.點出ation.models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="830b4-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="830b4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="830b4-138">OUTPUTS</span></span>

### <span data-ttu-id="830b4-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="830b4-139">System.Boolean</span></span>

## <span data-ttu-id="830b4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="830b4-140">NOTES</span></span>

## <span data-ttu-id="830b4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="830b4-141">RELATED LINKS</span></span>
