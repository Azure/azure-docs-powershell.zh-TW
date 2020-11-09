---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285688"
---
# <span data-ttu-id="4620e-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="4620e-101">New-AzAttestation</span></span>

## <span data-ttu-id="4620e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4620e-102">SYNOPSIS</span></span>
<span data-ttu-id="4620e-103">建立證明</span><span class="sxs-lookup"><span data-stu-id="4620e-103">Creates an attestation</span></span>

## <span data-ttu-id="4620e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4620e-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4620e-105">說明</span><span class="sxs-lookup"><span data-stu-id="4620e-105">DESCRIPTION</span></span>
<span data-ttu-id="4620e-106">New-AzAttestation Cmdlet 會在指定的資源群組中建立證明。</span><span class="sxs-lookup"><span data-stu-id="4620e-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="4620e-107">示例</span><span class="sxs-lookup"><span data-stu-id="4620e-107">EXAMPLES</span></span>

### <span data-ttu-id="4620e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4620e-108">Example 1</span></span>
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

<span data-ttu-id="4620e-109">使用幾個標籤建立名為 *pshtest4* 的證明提供者的新實例，並使用主機名稱 t 原則的 AAD 信任。</span><span class="sxs-lookup"><span data-stu-id="4620e-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="4620e-110">範例2</span><span class="sxs-lookup"><span data-stu-id="4620e-110">Example 2</span></span>
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

<span data-ttu-id="4620e-111">透過使用 PEM 檔案指定一組受信任的簽章金鑰，即可建立名為 *pshtest3* ' 的證明提供者的新實例，該實例使用的是 Isoladed 信任。</span><span class="sxs-lookup"><span data-stu-id="4620e-111">Create a new instance of an Attestation Provider named *pshtest3* \` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="4620e-112">參數</span><span class="sxs-lookup"><span data-stu-id="4620e-112">PARAMETERS</span></span>

### <span data-ttu-id="4620e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4620e-113">-DefaultProfile</span></span>
<span data-ttu-id="4620e-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4620e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4620e-115">-位置</span><span class="sxs-lookup"><span data-stu-id="4620e-115">-Location</span></span>
<span data-ttu-id="4620e-116">指定要在其中建立證明提供者的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="4620e-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="4620e-117">將命令 Get-AzResourceProvider 與 ProviderNamespace 參數搭配使用，即可查看您的選擇。</span><span class="sxs-lookup"><span data-stu-id="4620e-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="4620e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4620e-118">-Name</span></span>
<span data-ttu-id="4620e-119">指定要建立之實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="4620e-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="4620e-120">名稱可以是字母、數位或連字號的任何組合。</span><span class="sxs-lookup"><span data-stu-id="4620e-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="4620e-121">名稱必須以字母或數位開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="4620e-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="4620e-122">名稱必須是通用唯一的。</span><span class="sxs-lookup"><span data-stu-id="4620e-122">The name must be universally unique.</span></span>

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

### <span data-ttu-id="4620e-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="4620e-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="4620e-124">在單一憑證檔案中指定發行原則的信任簽章金鑰集合。</span><span class="sxs-lookup"><span data-stu-id="4620e-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

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

### <span data-ttu-id="4620e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4620e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4620e-126">指定要在其中建立證明之現有資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4620e-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

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

### <span data-ttu-id="4620e-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="4620e-127">-Tag</span></span>
<span data-ttu-id="4620e-128">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="4620e-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="4620e-129">-確認</span><span class="sxs-lookup"><span data-stu-id="4620e-129">-Confirm</span></span>
<span data-ttu-id="4620e-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4620e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4620e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4620e-131">-WhatIf</span></span>
<span data-ttu-id="4620e-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4620e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4620e-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4620e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4620e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4620e-134">CommonParameters</span></span>
<span data-ttu-id="4620e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4620e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4620e-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4620e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4620e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="4620e-137">INPUTS</span></span>

### <span data-ttu-id="4620e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="4620e-138">System.String</span></span>

### <span data-ttu-id="4620e-139">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4620e-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4620e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="4620e-140">OUTPUTS</span></span>

### <span data-ttu-id="4620e-141">PSAttestation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4620e-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="4620e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4620e-142">NOTES</span></span>

## <span data-ttu-id="4620e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="4620e-143">RELATED LINKS</span></span>
