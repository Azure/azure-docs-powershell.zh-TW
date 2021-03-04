---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: b628d93d44b863b4af05f09dd4d132ec986702e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905621"
---
# <span data-ttu-id="a203f-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="a203f-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="a203f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a203f-102">SYNOPSIS</span></span>
<span data-ttu-id="a203f-103">在 Azure 中重設租使用者中的策略。}</span><span class="sxs-lookup"><span data-stu-id="a203f-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="a203f-104">語法</span><span class="sxs-lookup"><span data-stu-id="a203f-104">SYNTAX</span></span>

### <span data-ttu-id="a203f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a203f-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a203f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a203f-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a203f-107">描述</span><span class="sxs-lookup"><span data-stu-id="a203f-107">DESCRIPTION</span></span>
<span data-ttu-id="a203f-108">Cmdlet Reset-AzAttestationPolicy Azure 的租使用者定義證明策略。</span><span class="sxs-lookup"><span data-stu-id="a203f-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="a203f-109">例子</span><span class="sxs-lookup"><span data-stu-id="a203f-109">EXAMPLES</span></span>

### <span data-ttu-id="a203f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="a203f-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="a203f-111">將 Tee 類型 *SgxEnclave* 之證明提供者 *pshtest* 的預設規則重設為預設值。</span><span class="sxs-lookup"><span data-stu-id="a203f-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="a203f-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="a203f-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="a203f-113">如果驗證提供者 *pshtest* 已設定為使用隔離信任模型，請包含已簽署之策略，將 Tee 類型 *SgxEnclave* 的預設值重設成預設。</span><span class="sxs-lookup"><span data-stu-id="a203f-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="a203f-114">參數</span><span class="sxs-lookup"><span data-stu-id="a203f-114">PARAMETERS</span></span>

### <span data-ttu-id="a203f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a203f-115">-DefaultProfile</span></span>
<span data-ttu-id="a203f-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a203f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a203f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a203f-117">-Name</span></span>
<span data-ttu-id="a203f-118">指定租使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="a203f-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="a203f-119">此 Cmdlet 會重設此參數指定的租使用者證明政策。</span><span class="sxs-lookup"><span data-stu-id="a203f-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="a203f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a203f-120">-PassThru</span></span>
<span data-ttu-id="a203f-121">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="a203f-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a203f-122">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="a203f-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a203f-123">-策略</span><span class="sxs-lookup"><span data-stu-id="a203f-123">-Policy</span></span>
<span data-ttu-id="a203f-124">指定描述要重設之政策檔的 JSON Web Token。</span><span class="sxs-lookup"><span data-stu-id="a203f-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="a203f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a203f-125">-ResourceGroupName</span></span>
<span data-ttu-id="a203f-126">指定驗證提供者的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a203f-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="a203f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a203f-127">-ResourceId</span></span>
<span data-ttu-id="a203f-128">指定證明提供者的 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="a203f-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="a203f-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="a203f-129">-Tee</span></span>
<span data-ttu-id="a203f-130">指定信任的執行環境類型。</span><span class="sxs-lookup"><span data-stu-id="a203f-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="a203f-131">我們支援四種類型的環境：SgxEnclave、OpenEnclave、CyResComponent 和 VBSEnclave。</span><span class="sxs-lookup"><span data-stu-id="a203f-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="a203f-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a203f-132">-Confirm</span></span>
<span data-ttu-id="a203f-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a203f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a203f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a203f-134">-WhatIf</span></span>
<span data-ttu-id="a203f-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a203f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a203f-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a203f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a203f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a203f-137">CommonParameters</span></span>
<span data-ttu-id="a203f-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a203f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a203f-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a203f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a203f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a203f-140">INPUTS</span></span>

### <span data-ttu-id="a203f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a203f-141">System.String</span></span>

## <span data-ttu-id="a203f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a203f-142">OUTPUTS</span></span>

### <span data-ttu-id="a203f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a203f-143">System.Boolean</span></span>

## <span data-ttu-id="a203f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a203f-144">NOTES</span></span>

## <span data-ttu-id="a203f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a203f-145">RELATED LINKS</span></span>
