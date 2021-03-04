---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c32a9e2fd474578c8526c8352e8649cb84d8b016
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905618"
---
# <span data-ttu-id="1ec42-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="1ec42-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="1ec42-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1ec42-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec42-103">在 Azure 標記法中設定租使用者中的策略。</span><span class="sxs-lookup"><span data-stu-id="1ec42-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="1ec42-104">語法</span><span class="sxs-lookup"><span data-stu-id="1ec42-104">SYNTAX</span></span>

### <span data-ttu-id="1ec42-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ec42-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ec42-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ec42-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ec42-107">描述</span><span class="sxs-lookup"><span data-stu-id="1ec42-107">DESCRIPTION</span></span>
<span data-ttu-id="1ec42-108">此Set-AzAttestationPolicy Cmdlet 會從 Azure 的租使用者中設定該策略。</span><span class="sxs-lookup"><span data-stu-id="1ec42-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="1ec42-109">例子</span><span class="sxs-lookup"><span data-stu-id="1ec42-109">EXAMPLES</span></span>

### <span data-ttu-id="1ec42-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="1ec42-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="1ec42-111">使用預設格式的文字策略格式設定 TEE 類型 *SgxEnclave* for *AShtest* (定義) 。</span><span class="sxs-lookup"><span data-stu-id="1ec42-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="1ec42-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="1ec42-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="1ec42-113">使用 JWT 策略格式設定 TEE 類型 *SgxEnclave* for證明提供者 *pshtest* 的使用者定義策略。</span><span class="sxs-lookup"><span data-stu-id="1ec42-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="1ec42-114">參數</span><span class="sxs-lookup"><span data-stu-id="1ec42-114">PARAMETERS</span></span>

### <span data-ttu-id="1ec42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec42-115">-DefaultProfile</span></span>
<span data-ttu-id="1ec42-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ec42-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ec42-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ec42-117">-Name</span></span>
<span data-ttu-id="1ec42-118">指定租使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ec42-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="1ec42-119">此 Cmdlet 會針對此參數指定的租使用者設定證明政策。</span><span class="sxs-lookup"><span data-stu-id="1ec42-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ec42-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ec42-120">-PassThru</span></span>
<span data-ttu-id="1ec42-121">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="1ec42-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1ec42-122">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="1ec42-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1ec42-123">-策略</span><span class="sxs-lookup"><span data-stu-id="1ec42-123">-Policy</span></span>
<span data-ttu-id="1ec42-124">指定要設定的政策檔。</span><span class="sxs-lookup"><span data-stu-id="1ec42-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="1ec42-125">此策略格式可以是文字或 JSON Web Token (JWT) 。</span><span class="sxs-lookup"><span data-stu-id="1ec42-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="1ec42-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="1ec42-126">-PolicyFormat</span></span>
<span data-ttu-id="1ec42-127">指定規則的格式，包括文字或 JWT (JSON Web Token) 。</span><span class="sxs-lookup"><span data-stu-id="1ec42-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="1ec42-128">預設政策格式為文字。</span><span class="sxs-lookup"><span data-stu-id="1ec42-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="1ec42-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec42-129">-ResourceGroupName</span></span>
<span data-ttu-id="1ec42-130">指定驗證提供者的資源組名。</span><span class="sxs-lookup"><span data-stu-id="1ec42-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="1ec42-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ec42-131">-ResourceId</span></span>
<span data-ttu-id="1ec42-132">指定證明提供者的 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="1ec42-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="1ec42-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="1ec42-133">-Tee</span></span>
<span data-ttu-id="1ec42-134">指定信任的執行環境類型。</span><span class="sxs-lookup"><span data-stu-id="1ec42-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="1ec42-135">支援四種環境類型：SgxEnclave、OpenEnclave、CyResComponent 和 VBSEnclave。</span><span class="sxs-lookup"><span data-stu-id="1ec42-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="1ec42-136">-確認</span><span class="sxs-lookup"><span data-stu-id="1ec42-136">-Confirm</span></span>
<span data-ttu-id="1ec42-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1ec42-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec42-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec42-138">-WhatIf</span></span>
<span data-ttu-id="1ec42-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ec42-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec42-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ec42-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec42-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec42-141">CommonParameters</span></span>
<span data-ttu-id="1ec42-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1ec42-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec42-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ec42-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec42-144">輸入</span><span class="sxs-lookup"><span data-stu-id="1ec42-144">INPUTS</span></span>

### <span data-ttu-id="1ec42-145">System.String</span><span class="sxs-lookup"><span data-stu-id="1ec42-145">System.String</span></span>

## <span data-ttu-id="1ec42-146">輸出</span><span class="sxs-lookup"><span data-stu-id="1ec42-146">OUTPUTS</span></span>

### <span data-ttu-id="1ec42-147">System.String</span><span class="sxs-lookup"><span data-stu-id="1ec42-147">System.String</span></span>

## <span data-ttu-id="1ec42-148">筆記</span><span class="sxs-lookup"><span data-stu-id="1ec42-148">NOTES</span></span>

## <span data-ttu-id="1ec42-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ec42-149">RELATED LINKS</span></span>
