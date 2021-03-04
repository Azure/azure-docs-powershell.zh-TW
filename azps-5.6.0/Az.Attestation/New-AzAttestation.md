---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: 1fbb3c5d1a82261f5c25bd4351aabcb838355bda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913978"
---
# <span data-ttu-id="f0ce4-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="f0ce4-101">New-AzAttestation</span></span>

## <span data-ttu-id="f0ce4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ce4-103">建立證明</span><span class="sxs-lookup"><span data-stu-id="f0ce4-103">Creates an attestation</span></span>

## <span data-ttu-id="f0ce4-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0ce4-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0ce4-105">描述</span><span class="sxs-lookup"><span data-stu-id="f0ce4-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ce4-106">Cmdlet New-AzAttestation指定資源群組中建立證明。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="f0ce4-107">例子</span><span class="sxs-lookup"><span data-stu-id="f0ce4-107">EXAMPLES</span></span>

### <span data-ttu-id="f0ce4-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f0ce4-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest4 -ResourceGroupName psh-test-rg -Location "East US" -Tags @{Test="true";CreationYear="2020"}                                                                                                                                                                                         
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest4
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest4
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest4.us.attest.azure.net
Tags              : {CreationYear, Test}
TagsTable         :
                    Name          Value
                    ============  =====
                    CreationYear  2020
                    Test          true
```

<span data-ttu-id="f0ce4-109">使用幾個標記，使用 AAD 信任來主控 TEE 政策，以建立一個名為 *pshtest4* 的認證提供者新實例。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="f0ce4-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="f0ce4-110">Example 2</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg -Location "East US" -PolicySignersCertificateFile .\cert1.pem                                                                                                                                                
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest3
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest3
Status            : Ready
TrustModel        : Isolated
AttestUri         : https://pshtest3.us.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="f0ce4-111">建立名為 *pshtest3*' 的檢定提供者新實例，此實例使用 Isoladed 信任，透過 PEM 檔案指定一組信任的簽署金鑰，以主控 TEE 策略。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-111">Create a new instance of an Attestation Provider named *pshtest3*\` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="f0ce4-112">參數</span><span class="sxs-lookup"><span data-stu-id="f0ce4-112">PARAMETERS</span></span>

### <span data-ttu-id="f0ce4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ce4-113">-DefaultProfile</span></span>
<span data-ttu-id="f0ce4-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ce4-115">-位置</span><span class="sxs-lookup"><span data-stu-id="f0ce4-115">-Location</span></span>
<span data-ttu-id="f0ce4-116">指定要建立證明提供者的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="f0ce4-117">使用Get-AzResourceProvider ProviderNamespace 參數來查看您的選擇。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ce4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0ce4-118">-Name</span></span>
<span data-ttu-id="f0ce4-119">指定要建立的實例名稱。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="f0ce4-120">名稱可以是字母、數位或連字號的任何組合。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="f0ce4-121">名稱必須以字母或數位做為開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="f0ce4-122">名稱必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-122">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ce4-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="f0ce4-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="f0ce4-124">指定單一憑證檔案中發佈策略的一組信任簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ce4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ce4-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0ce4-126">指定要建立證明之現有資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ce4-127">-標記</span><span class="sxs-lookup"><span data-stu-id="f0ce4-127">-Tag</span></span>
<span data-ttu-id="f0ce4-128">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ce4-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f0ce4-129">-Confirm</span></span>
<span data-ttu-id="f0ce4-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0ce4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ce4-131">-WhatIf</span></span>
<span data-ttu-id="f0ce4-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0ce4-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0ce4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ce4-134">CommonParameters</span></span>
<span data-ttu-id="f0ce4-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0ce4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ce4-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0ce4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ce4-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f0ce4-137">INPUTS</span></span>

### <span data-ttu-id="f0ce4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f0ce4-138">System.String</span></span>

### <span data-ttu-id="f0ce4-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f0ce4-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f0ce4-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f0ce4-140">OUTPUTS</span></span>

### <span data-ttu-id="f0ce4-141">Microsoft.Azure.Commands.點出ation.models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="f0ce4-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="f0ce4-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f0ce4-142">NOTES</span></span>

## <span data-ttu-id="f0ce4-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0ce4-143">RELATED LINKS</span></span>
