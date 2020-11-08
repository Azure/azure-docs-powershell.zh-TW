---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126584"
---
# <span data-ttu-id="60e13-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="60e13-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="60e13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60e13-102">SYNOPSIS</span></span>
<span data-ttu-id="60e13-103">在 Azure Attestationn 中設定租使用者的原則。</span><span class="sxs-lookup"><span data-stu-id="60e13-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="60e13-104">句法</span><span class="sxs-lookup"><span data-stu-id="60e13-104">SYNTAX</span></span>

### <span data-ttu-id="60e13-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="60e13-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60e13-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60e13-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60e13-107">說明</span><span class="sxs-lookup"><span data-stu-id="60e13-107">DESCRIPTION</span></span>
<span data-ttu-id="60e13-108">Set-AzAttestationPolicy Cmdlet 會從 Azure 證明中的租使用者設定原則。</span><span class="sxs-lookup"><span data-stu-id="60e13-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="60e13-109">示例</span><span class="sxs-lookup"><span data-stu-id="60e13-109">EXAMPLES</span></span>

### <span data-ttu-id="60e13-110">範例1</span><span class="sxs-lookup"><span data-stu-id="60e13-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="60e13-111">*針對認證* 提供者 *pshtest* 使用 (預設) 的文字原則格式，設定使用者定義的原則。</span><span class="sxs-lookup"><span data-stu-id="60e13-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="60e13-112">範例2</span><span class="sxs-lookup"><span data-stu-id="60e13-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="60e13-113">針對認證提供者 *pshtest* 使用 JWT 原則格式，為其 t 型類型 *SgxEnclave* 設定使用者定義的原則。</span><span class="sxs-lookup"><span data-stu-id="60e13-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="60e13-114">參數</span><span class="sxs-lookup"><span data-stu-id="60e13-114">PARAMETERS</span></span>

### <span data-ttu-id="60e13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e13-115">-DefaultProfile</span></span>
<span data-ttu-id="60e13-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60e13-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e13-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="60e13-117">-Name</span></span>
<span data-ttu-id="60e13-118">指定租使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="60e13-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="60e13-119">這個 Cmdlet 會針對此參數指定的租使用者設定認證原則。</span><span class="sxs-lookup"><span data-stu-id="60e13-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="60e13-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60e13-120">-PassThru</span></span>
<span data-ttu-id="60e13-121">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="60e13-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="60e13-122">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="60e13-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="60e13-123">-原則</span><span class="sxs-lookup"><span data-stu-id="60e13-123">-Policy</span></span>
<span data-ttu-id="60e13-124">指定要設定的原則檔。</span><span class="sxs-lookup"><span data-stu-id="60e13-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="60e13-125">原則格式可以是 Text 或 JSON Web 權杖 (JWT) 。</span><span class="sxs-lookup"><span data-stu-id="60e13-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="60e13-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="60e13-126">-PolicyFormat</span></span>
<span data-ttu-id="60e13-127">指定原則的格式，例如 [文字] 或 [JWT (JSON Web 權杖]) 。</span><span class="sxs-lookup"><span data-stu-id="60e13-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="60e13-128">預設原則格式為 [文字]。</span><span class="sxs-lookup"><span data-stu-id="60e13-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="60e13-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60e13-129">-ResourceGroupName</span></span>
<span data-ttu-id="60e13-130">指定證明提供者的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="60e13-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="60e13-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60e13-131">-ResourceId</span></span>
<span data-ttu-id="60e13-132">指定證明提供者的 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="60e13-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="60e13-133">-T</span><span class="sxs-lookup"><span data-stu-id="60e13-133">-Tee</span></span>
<span data-ttu-id="60e13-134">指定信任的執行環境類型。</span><span class="sxs-lookup"><span data-stu-id="60e13-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="60e13-135">支援四種類型的環境： SgxEnclave、OpenEnclave、CyResComponent 和 VBSEnclave。</span><span class="sxs-lookup"><span data-stu-id="60e13-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="60e13-136">-確認</span><span class="sxs-lookup"><span data-stu-id="60e13-136">-Confirm</span></span>
<span data-ttu-id="60e13-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60e13-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60e13-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e13-138">-WhatIf</span></span>
<span data-ttu-id="60e13-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60e13-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60e13-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60e13-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60e13-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e13-141">CommonParameters</span></span>
<span data-ttu-id="60e13-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60e13-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e13-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="60e13-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e13-144">輸入</span><span class="sxs-lookup"><span data-stu-id="60e13-144">INPUTS</span></span>

### <span data-ttu-id="60e13-145">System.object</span><span class="sxs-lookup"><span data-stu-id="60e13-145">System.String</span></span>

## <span data-ttu-id="60e13-146">輸出</span><span class="sxs-lookup"><span data-stu-id="60e13-146">OUTPUTS</span></span>

### <span data-ttu-id="60e13-147">System.object</span><span class="sxs-lookup"><span data-stu-id="60e13-147">System.String</span></span>

## <span data-ttu-id="60e13-148">筆記</span><span class="sxs-lookup"><span data-stu-id="60e13-148">NOTES</span></span>

## <span data-ttu-id="60e13-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="60e13-149">RELATED LINKS</span></span>
