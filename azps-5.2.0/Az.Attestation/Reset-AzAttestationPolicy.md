---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280740"
---
# <span data-ttu-id="9400b-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="9400b-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="9400b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9400b-102">SYNOPSIS</span></span>
<span data-ttu-id="9400b-103">在 Azure Attestationn 中重設租使用者的原則。</span><span class="sxs-lookup"><span data-stu-id="9400b-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="9400b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9400b-104">SYNTAX</span></span>

### <span data-ttu-id="9400b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9400b-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9400b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9400b-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9400b-107">說明</span><span class="sxs-lookup"><span data-stu-id="9400b-107">DESCRIPTION</span></span>
<span data-ttu-id="9400b-108">Reset-AzAttestationPolicy Cmdlet 會從 Azure 證明中的租使用者重設使用者定義的證明原則。</span><span class="sxs-lookup"><span data-stu-id="9400b-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="9400b-109">示例</span><span class="sxs-lookup"><span data-stu-id="9400b-109">EXAMPLES</span></span>

### <span data-ttu-id="9400b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9400b-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="9400b-111">針對 t 類型 *SgxEnclave* 的認證提供者 *pshtest* ，將原則重設為預設值。</span><span class="sxs-lookup"><span data-stu-id="9400b-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="9400b-112">範例2</span><span class="sxs-lookup"><span data-stu-id="9400b-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="9400b-113">如果認證提供者 *pshtest* 已設定為使用隔離信任模型，請在包含簽署原則的情況下，將原則重設為 t 類型 *SgxEnclave* 的預設值。</span><span class="sxs-lookup"><span data-stu-id="9400b-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="9400b-114">參數</span><span class="sxs-lookup"><span data-stu-id="9400b-114">PARAMETERS</span></span>

### <span data-ttu-id="9400b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9400b-115">-DefaultProfile</span></span>
<span data-ttu-id="9400b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9400b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9400b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9400b-117">-Name</span></span>
<span data-ttu-id="9400b-118">指定租使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9400b-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="9400b-119">這個 Cmdlet 會針對此參數指定的租使用者重設認證原則。</span><span class="sxs-lookup"><span data-stu-id="9400b-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9400b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9400b-120">-PassThru</span></span>
<span data-ttu-id="9400b-121">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="9400b-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9400b-122">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="9400b-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9400b-123">-原則</span><span class="sxs-lookup"><span data-stu-id="9400b-123">-Policy</span></span>
<span data-ttu-id="9400b-124">指定用於描述要重設之原則檔的 JSON Web 權杖。</span><span class="sxs-lookup"><span data-stu-id="9400b-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9400b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9400b-125">-ResourceGroupName</span></span>
<span data-ttu-id="9400b-126">指定證明提供者的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9400b-126">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9400b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9400b-127">-ResourceId</span></span>
<span data-ttu-id="9400b-128">指定證明提供者的 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="9400b-128">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9400b-129">-T</span><span class="sxs-lookup"><span data-stu-id="9400b-129">-Tee</span></span>
<span data-ttu-id="9400b-130">指定信任的執行環境類型。</span><span class="sxs-lookup"><span data-stu-id="9400b-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="9400b-131">我們支援四種類型的環境： SgxEnclave、OpenEnclave、CyResComponent 和 VBSEnclave。</span><span class="sxs-lookup"><span data-stu-id="9400b-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="9400b-132">-確認</span><span class="sxs-lookup"><span data-stu-id="9400b-132">-Confirm</span></span>
<span data-ttu-id="9400b-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9400b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9400b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9400b-134">-WhatIf</span></span>
<span data-ttu-id="9400b-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9400b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9400b-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9400b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9400b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9400b-137">CommonParameters</span></span>
<span data-ttu-id="9400b-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9400b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9400b-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9400b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9400b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="9400b-140">INPUTS</span></span>

### <span data-ttu-id="9400b-141">System.object</span><span class="sxs-lookup"><span data-stu-id="9400b-141">System.String</span></span>

## <span data-ttu-id="9400b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9400b-142">OUTPUTS</span></span>

### <span data-ttu-id="9400b-143">System.object</span><span class="sxs-lookup"><span data-stu-id="9400b-143">System.Boolean</span></span>

## <span data-ttu-id="9400b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9400b-144">NOTES</span></span>

## <span data-ttu-id="9400b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9400b-145">RELATED LINKS</span></span>
