---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssvaultcertificateconfig
schema: 2.0.0
ms.openlocfilehash: 9ae4e22cde856129d21965b7e7f2fc9af647572a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801757"
---
# <span data-ttu-id="d3470-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="d3470-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="d3470-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3470-102">SYNOPSIS</span></span>
<span data-ttu-id="d3470-103">建立金鑰 Vault 憑證設定。</span><span class="sxs-lookup"><span data-stu-id="d3470-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3470-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3470-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3470-105">說明</span><span class="sxs-lookup"><span data-stu-id="d3470-105">DESCRIPTION</span></span>
<span data-ttu-id="d3470-106">**新的-AzureRmVmssVaultCertificateConfig** Cmdlet 會指定必須放在虛擬機器縮放集 (VMSS) 虛擬機器上的機密。</span><span class="sxs-lookup"><span data-stu-id="d3470-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="d3470-107">這個 Cmdlet 的輸出應該與 Add-AzureRmVmssSecret Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d3470-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="d3470-108">示例</span><span class="sxs-lookup"><span data-stu-id="d3470-108">EXAMPLES</span></span>

### <span data-ttu-id="d3470-109">範例1：建立主要電子倉庫憑證設定</span><span class="sxs-lookup"><span data-stu-id="d3470-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="d3470-110">這個命令會建立一個主要的電子倉庫憑證配置，該設定會使用位於指定憑證 URL 之名為 MyCerts 的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="d3470-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="d3470-111">參數</span><span class="sxs-lookup"><span data-stu-id="d3470-111">PARAMETERS</span></span>

### <span data-ttu-id="d3470-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="d3470-112">-CertificateStore</span></span>
<span data-ttu-id="d3470-113">在新增憑證的規模集中，指定虛擬機器上的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="d3470-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="d3470-114">這僅適用于 Windows 虛擬電腦縮放集。</span><span class="sxs-lookup"><span data-stu-id="d3470-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="d3470-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="d3470-115">-CertificateUrl</span></span>
<span data-ttu-id="d3470-116">指定儲存在金鑰儲存庫中之憑證的 URI。</span><span class="sxs-lookup"><span data-stu-id="d3470-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="d3470-117">它是以 UTF-8 編碼的下列 JSON 物件的 base64 編碼：</span><span class="sxs-lookup"><span data-stu-id="d3470-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="d3470-118">{"data"： " \<Base64-encoded-certificate\> "，"資料類型"： "pfx"，"password"： " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="d3470-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="d3470-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3470-119">-DefaultProfile</span></span>
<span data-ttu-id="d3470-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3470-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3470-121">-確認</span><span class="sxs-lookup"><span data-stu-id="d3470-121">-Confirm</span></span>
<span data-ttu-id="d3470-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3470-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3470-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3470-123">-WhatIf</span></span>
<span data-ttu-id="d3470-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3470-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3470-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3470-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3470-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3470-126">CommonParameters</span></span>
<span data-ttu-id="d3470-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3470-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3470-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d3470-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3470-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d3470-129">INPUTS</span></span>

### <span data-ttu-id="d3470-130">所有</span><span class="sxs-lookup"><span data-stu-id="d3470-130">None</span></span>
<span data-ttu-id="d3470-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d3470-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d3470-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d3470-132">OUTPUTS</span></span>

###  
<span data-ttu-id="d3470-133">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d3470-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d3470-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d3470-134">NOTES</span></span>

## <span data-ttu-id="d3470-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3470-135">RELATED LINKS</span></span>

[<span data-ttu-id="d3470-136">附加 AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="d3470-136">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
