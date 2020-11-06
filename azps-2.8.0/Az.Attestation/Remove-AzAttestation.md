---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 997e1150549ac219c54e42fdd4c7674cd53d5ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613824"
---
# <span data-ttu-id="a6c1c-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="a6c1c-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="a6c1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c1c-103">刪除證明。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-103">Deletes an attestation.</span></span>

## <span data-ttu-id="a6c1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6c1c-104">SYNTAX</span></span>

### <span data-ttu-id="a6c1c-105">ByAvailableAttestation (預設) </span><span class="sxs-lookup"><span data-stu-id="a6c1c-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c1c-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="a6c1c-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c1c-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="a6c1c-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6c1c-108">說明</span><span class="sxs-lookup"><span data-stu-id="a6c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="a6c1c-109">Remove-AzAttestation Cmdlet 會刪除指定的認證。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="a6c1c-110">示例</span><span class="sxs-lookup"><span data-stu-id="a6c1c-110">EXAMPLES</span></span>

### <span data-ttu-id="a6c1c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a6c1c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name example -ResourceGroupName rg1 
```

<span data-ttu-id="a6c1c-112">從目前的訂閱和資源群組 "rg1" 刪除證明「範例」。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-112">Delete Attestation "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="a6c1c-113">參數</span><span class="sxs-lookup"><span data-stu-id="a6c1c-113">PARAMETERS</span></span>

### <span data-ttu-id="a6c1c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6c1c-114">-AsJob</span></span>
<span data-ttu-id="a6c1c-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6c1c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6c1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c1c-116">-DefaultProfile</span></span>
<span data-ttu-id="a6c1c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6c1c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6c1c-118">-InputObject</span></span>
<span data-ttu-id="a6c1c-119">要刪除的證明物件。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-119">Attestation object to be deleted.</span></span>

```yaml
Type: PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6c1c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6c1c-120">-Name</span></span>
<span data-ttu-id="a6c1c-121">指定要移除認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-121">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c1c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6c1c-122">-PassThru</span></span>
<span data-ttu-id="a6c1c-123">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a6c1c-124">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a6c1c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c1c-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6c1c-126">指定要移除之 Azure 證明的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-126">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c1c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6c1c-127">-ResourceId</span></span>
<span data-ttu-id="a6c1c-128">證明資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-128">Attestation Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6c1c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a6c1c-129">-Confirm</span></span>
<span data-ttu-id="a6c1c-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6c1c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c1c-131">-WhatIf</span></span>
<span data-ttu-id="a6c1c-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c1c-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6c1c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c1c-134">CommonParameters</span></span>
<span data-ttu-id="a6c1c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c1c-136">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a6c1c-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c1c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a6c1c-137">INPUTS</span></span>

### <span data-ttu-id="a6c1c-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a6c1c-138">System.String</span></span>

### <span data-ttu-id="a6c1c-139">PSAttestation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a6c1c-139">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="a6c1c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a6c1c-140">OUTPUTS</span></span>

### <span data-ttu-id="a6c1c-141">System.object</span><span class="sxs-lookup"><span data-stu-id="a6c1c-141">System.Boolean</span></span>

## <span data-ttu-id="a6c1c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a6c1c-142">NOTES</span></span>

## <span data-ttu-id="a6c1c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6c1c-143">RELATED LINKS</span></span>
