---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 9014c91626d41e66f316b870e042af7d5655f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450684"
---
# <span data-ttu-id="21edc-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="21edc-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="21edc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21edc-102">SYNOPSIS</span></span>
<span data-ttu-id="21edc-103">建立金鑰 Vault 憑證設定。</span><span class="sxs-lookup"><span data-stu-id="21edc-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21edc-104">句法</span><span class="sxs-lookup"><span data-stu-id="21edc-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21edc-105">說明</span><span class="sxs-lookup"><span data-stu-id="21edc-105">DESCRIPTION</span></span>
<span data-ttu-id="21edc-106">**新的-AzureRmVmssVaultCertificateConfig** Cmdlet 會指定必須放在虛擬機器縮放集 (VMSS) 虛擬機器上的機密。</span><span class="sxs-lookup"><span data-stu-id="21edc-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="21edc-107">這個 Cmdlet 的輸出應該與 Add-AzureRmVmssSecret Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="21edc-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="21edc-108">示例</span><span class="sxs-lookup"><span data-stu-id="21edc-108">EXAMPLES</span></span>

### <span data-ttu-id="21edc-109">範例1：建立主要電子倉庫憑證設定</span><span class="sxs-lookup"><span data-stu-id="21edc-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="21edc-110">這個命令會建立一個主要的電子倉庫憑證配置，該設定會使用位於指定憑證 URL 之名為 MyCerts 的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="21edc-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="21edc-111">參數</span><span class="sxs-lookup"><span data-stu-id="21edc-111">PARAMETERS</span></span>

### <span data-ttu-id="21edc-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="21edc-112">-CertificateStore</span></span>
<span data-ttu-id="21edc-113">在新增憑證的規模集中，指定虛擬機器上的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="21edc-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="21edc-114">這僅適用于 Windows 虛擬電腦縮放集。</span><span class="sxs-lookup"><span data-stu-id="21edc-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21edc-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="21edc-115">-CertificateUrl</span></span>
<span data-ttu-id="21edc-116">指定儲存在金鑰儲存庫中之憑證的 URI。</span><span class="sxs-lookup"><span data-stu-id="21edc-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="21edc-117">它是以 UTF-8 編碼的下列 JSON 物件的 base64 編碼：</span><span class="sxs-lookup"><span data-stu-id="21edc-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="21edc-118">{"data"： " \<Base64-encoded-certificate\> "，"資料類型"： "pfx"，"password"： " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="21edc-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21edc-119">-確認</span><span class="sxs-lookup"><span data-stu-id="21edc-119">-Confirm</span></span>
<span data-ttu-id="21edc-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21edc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21edc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21edc-121">-WhatIf</span></span>
<span data-ttu-id="21edc-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21edc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21edc-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21edc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21edc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21edc-124">CommonParameters</span></span>
<span data-ttu-id="21edc-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21edc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21edc-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21edc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21edc-127">輸入</span><span class="sxs-lookup"><span data-stu-id="21edc-127">INPUTS</span></span>

### <span data-ttu-id="21edc-128">所有</span><span class="sxs-lookup"><span data-stu-id="21edc-128">None</span></span>
<span data-ttu-id="21edc-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="21edc-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21edc-130">輸出</span><span class="sxs-lookup"><span data-stu-id="21edc-130">OUTPUTS</span></span>

###  
<span data-ttu-id="21edc-131">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="21edc-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="21edc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="21edc-132">NOTES</span></span>

## <span data-ttu-id="21edc-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="21edc-133">RELATED LINKS</span></span>

[<span data-ttu-id="21edc-134">附加 AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="21edc-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
