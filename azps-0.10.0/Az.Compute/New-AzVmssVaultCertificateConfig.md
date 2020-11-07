---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 0889bfa5abfdf90480eb508ebad7a62607912722
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796094"
---
# <span data-ttu-id="58ddc-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="58ddc-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="58ddc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="58ddc-103">建立金鑰 Vault 憑證設定。</span><span class="sxs-lookup"><span data-stu-id="58ddc-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="58ddc-104">句法</span><span class="sxs-lookup"><span data-stu-id="58ddc-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ddc-105">說明</span><span class="sxs-lookup"><span data-stu-id="58ddc-105">DESCRIPTION</span></span>
<span data-ttu-id="58ddc-106">**新的-AzVmssVaultCertificateConfig** Cmdlet 會指定必須放在虛擬機器縮放集 (VMSS) 虛擬機器上的機密。</span><span class="sxs-lookup"><span data-stu-id="58ddc-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="58ddc-107">這個 Cmdlet 的輸出應該與 Add-AzVmssSecret Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="58ddc-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="58ddc-108">示例</span><span class="sxs-lookup"><span data-stu-id="58ddc-108">EXAMPLES</span></span>

### <span data-ttu-id="58ddc-109">範例1：建立主要電子倉庫憑證設定</span><span class="sxs-lookup"><span data-stu-id="58ddc-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="58ddc-110">這個命令會建立一個主要的電子倉庫憑證配置，該設定會使用位於指定憑證 URL 之名為 MyCerts 的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="58ddc-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="58ddc-111">參數</span><span class="sxs-lookup"><span data-stu-id="58ddc-111">PARAMETERS</span></span>

### <span data-ttu-id="58ddc-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="58ddc-112">-CertificateStore</span></span>
<span data-ttu-id="58ddc-113">在新增憑證的規模集中，指定虛擬機器上的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="58ddc-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="58ddc-114">這僅適用于 Windows 虛擬電腦縮放集。</span><span class="sxs-lookup"><span data-stu-id="58ddc-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="58ddc-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="58ddc-115">-CertificateUrl</span></span>
<span data-ttu-id="58ddc-116">指定儲存在金鑰儲存庫中之憑證的 URI。</span><span class="sxs-lookup"><span data-stu-id="58ddc-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="58ddc-117">它是以 UTF-8 編碼的下列 JSON 物件的 base64 編碼：</span><span class="sxs-lookup"><span data-stu-id="58ddc-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="58ddc-118">{「資料」： \< 」Base64 編碼-憑證 \> "，" dataType "：" pfx "，" 密碼 "：" \< pfx-檔案-密碼 \> "}</span><span class="sxs-lookup"><span data-stu-id="58ddc-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="58ddc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ddc-119">-DefaultProfile</span></span>
<span data-ttu-id="58ddc-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58ddc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58ddc-121">-確認</span><span class="sxs-lookup"><span data-stu-id="58ddc-121">-Confirm</span></span>
<span data-ttu-id="58ddc-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58ddc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ddc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ddc-123">-WhatIf</span></span>
<span data-ttu-id="58ddc-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58ddc-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58ddc-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58ddc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ddc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ddc-126">CommonParameters</span></span>
<span data-ttu-id="58ddc-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58ddc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ddc-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58ddc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ddc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="58ddc-129">INPUTS</span></span>

### <span data-ttu-id="58ddc-130">所有</span><span class="sxs-lookup"><span data-stu-id="58ddc-130">None</span></span>
<span data-ttu-id="58ddc-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="58ddc-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58ddc-132">輸出</span><span class="sxs-lookup"><span data-stu-id="58ddc-132">OUTPUTS</span></span>

###  
<span data-ttu-id="58ddc-133">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="58ddc-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="58ddc-134">筆記</span><span class="sxs-lookup"><span data-stu-id="58ddc-134">NOTES</span></span>

## <span data-ttu-id="58ddc-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="58ddc-135">RELATED LINKS</span></span>

[<span data-ttu-id="58ddc-136">附加 AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="58ddc-136">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
