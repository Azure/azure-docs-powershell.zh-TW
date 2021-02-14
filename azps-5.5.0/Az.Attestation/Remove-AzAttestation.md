---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130123"
---
# <span data-ttu-id="64ac9-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="64ac9-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="64ac9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="64ac9-103">刪除證明。</span><span class="sxs-lookup"><span data-stu-id="64ac9-103">Deletes an attestation.</span></span>

## <span data-ttu-id="64ac9-104">句法</span><span class="sxs-lookup"><span data-stu-id="64ac9-104">SYNTAX</span></span>

### <span data-ttu-id="64ac9-105">ByAvailableAttestation (預設) </span><span class="sxs-lookup"><span data-stu-id="64ac9-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64ac9-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="64ac9-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64ac9-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="64ac9-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64ac9-108">說明</span><span class="sxs-lookup"><span data-stu-id="64ac9-108">DESCRIPTION</span></span>
<span data-ttu-id="64ac9-109">Remove-AzAttestation Cmdlet 會刪除指定的認證。</span><span class="sxs-lookup"><span data-stu-id="64ac9-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="64ac9-110">示例</span><span class="sxs-lookup"><span data-stu-id="64ac9-110">EXAMPLES</span></span>

### <span data-ttu-id="64ac9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="64ac9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="64ac9-112">在名為 [ *psh* ] 的資源群組中，從目前的訂閱刪除名為 *Pshtest3* 的證明提供者。</span><span class="sxs-lookup"><span data-stu-id="64ac9-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="64ac9-113">參數</span><span class="sxs-lookup"><span data-stu-id="64ac9-113">PARAMETERS</span></span>

### <span data-ttu-id="64ac9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ac9-114">-DefaultProfile</span></span>
<span data-ttu-id="64ac9-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64ac9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ac9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64ac9-116">-InputObject</span></span>
<span data-ttu-id="64ac9-117">要刪除的證明物件。</span><span class="sxs-lookup"><span data-stu-id="64ac9-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="64ac9-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="64ac9-118">-Name</span></span>
<span data-ttu-id="64ac9-119">指定要移除認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ac9-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="64ac9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64ac9-120">-PassThru</span></span>
<span data-ttu-id="64ac9-121">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="64ac9-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="64ac9-122">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="64ac9-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="64ac9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ac9-123">-ResourceGroupName</span></span>
<span data-ttu-id="64ac9-124">指定要移除之 Azure 證明的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ac9-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="64ac9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64ac9-125">-ResourceId</span></span>
<span data-ttu-id="64ac9-126">證明資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="64ac9-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="64ac9-127">-確認</span><span class="sxs-lookup"><span data-stu-id="64ac9-127">-Confirm</span></span>
<span data-ttu-id="64ac9-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64ac9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64ac9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64ac9-129">-WhatIf</span></span>
<span data-ttu-id="64ac9-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64ac9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64ac9-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64ac9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64ac9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ac9-132">CommonParameters</span></span>
<span data-ttu-id="64ac9-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64ac9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ac9-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="64ac9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ac9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="64ac9-135">INPUTS</span></span>

### <span data-ttu-id="64ac9-136">System.object</span><span class="sxs-lookup"><span data-stu-id="64ac9-136">System.String</span></span>

### <span data-ttu-id="64ac9-137">PSAttestation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="64ac9-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="64ac9-138">輸出</span><span class="sxs-lookup"><span data-stu-id="64ac9-138">OUTPUTS</span></span>

### <span data-ttu-id="64ac9-139">System.object</span><span class="sxs-lookup"><span data-stu-id="64ac9-139">System.Boolean</span></span>

## <span data-ttu-id="64ac9-140">筆記</span><span class="sxs-lookup"><span data-stu-id="64ac9-140">NOTES</span></span>

## <span data-ttu-id="64ac9-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="64ac9-141">RELATED LINKS</span></span>
