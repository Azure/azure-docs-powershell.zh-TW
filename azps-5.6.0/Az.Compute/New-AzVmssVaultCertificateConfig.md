---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: cc607e12873e0b5b738a64d781d16ed73bc72f7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911166"
---
# <span data-ttu-id="304a1-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="304a1-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="304a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="304a1-102">SYNOPSIS</span></span>
<span data-ttu-id="304a1-103">建立金鑰保存庫憑證組狀。</span><span class="sxs-lookup"><span data-stu-id="304a1-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="304a1-104">語法</span><span class="sxs-lookup"><span data-stu-id="304a1-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="304a1-105">描述</span><span class="sxs-lookup"><span data-stu-id="304a1-105">DESCRIPTION</span></span>
<span data-ttu-id="304a1-106">**New-Az VmssVaultCertificateConfig** Cmdlet 指定虛擬機器的虛擬機器縮放集 (VMSS) 中必須放置的秘訣。</span><span class="sxs-lookup"><span data-stu-id="304a1-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="304a1-107">此 Cmdlet 的輸出旨在與 Add-AzVmssSecret 一起使用。</span><span class="sxs-lookup"><span data-stu-id="304a1-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="304a1-108">例子</span><span class="sxs-lookup"><span data-stu-id="304a1-108">EXAMPLES</span></span>

### <span data-ttu-id="304a1-109">範例 1：建立金鑰保存庫憑證組</span><span class="sxs-lookup"><span data-stu-id="304a1-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="304a1-110">此命令會建立使用名稱為 MyCerts 的憑證存放區 ，位於指定憑證 URL 的金鑰保存庫憑證組。</span><span class="sxs-lookup"><span data-stu-id="304a1-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="304a1-111">參數</span><span class="sxs-lookup"><span data-stu-id="304a1-111">PARAMETERS</span></span>

### <span data-ttu-id="304a1-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="304a1-112">-CertificateStore</span></span>
<span data-ttu-id="304a1-113">指定新增憑證之縮放集虛擬機器上的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="304a1-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="304a1-114">這僅適用于 Windows 虛擬機器縮放集。</span><span class="sxs-lookup"><span data-stu-id="304a1-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="304a1-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="304a1-115">-CertificateUrl</span></span>
<span data-ttu-id="304a1-116">指定儲存在金鑰保存庫中之憑證的 URI。</span><span class="sxs-lookup"><span data-stu-id="304a1-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="304a1-117">它是下列 JSON 物件的基本編碼，編碼為 UTF-8：{ "data"：" \<Base64-encoded-certificate\> "， "dataType"："pfx"， "password"：" \<pfx-file-password\> " }</span><span class="sxs-lookup"><span data-stu-id="304a1-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="304a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304a1-118">-DefaultProfile</span></span>
<span data-ttu-id="304a1-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="304a1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="304a1-120">-確認</span><span class="sxs-lookup"><span data-stu-id="304a1-120">-Confirm</span></span>
<span data-ttu-id="304a1-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="304a1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="304a1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="304a1-122">-WhatIf</span></span>
<span data-ttu-id="304a1-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="304a1-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="304a1-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="304a1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="304a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304a1-125">CommonParameters</span></span>
<span data-ttu-id="304a1-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="304a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304a1-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="304a1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304a1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="304a1-128">INPUTS</span></span>

### <span data-ttu-id="304a1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="304a1-129">System.String</span></span>

## <span data-ttu-id="304a1-130">輸出</span><span class="sxs-lookup"><span data-stu-id="304a1-130">OUTPUTS</span></span>

### <span data-ttu-id="304a1-131">Microsoft.Azure.management.Compute.models.VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="304a1-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="304a1-132">筆記</span><span class="sxs-lookup"><span data-stu-id="304a1-132">NOTES</span></span>

## <span data-ttu-id="304a1-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="304a1-133">RELATED LINKS</span></span>

[<span data-ttu-id="304a1-134">Add-AzEvssSecret</span><span class="sxs-lookup"><span data-stu-id="304a1-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
