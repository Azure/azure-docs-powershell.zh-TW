---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: d0f9e69ff36348cb4eb49920b85709b9b268adf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625345"
---
# <span data-ttu-id="12518-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="12518-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="12518-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12518-102">SYNOPSIS</span></span>
<span data-ttu-id="12518-103">建立金鑰 Vault 憑證設定。</span><span class="sxs-lookup"><span data-stu-id="12518-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12518-104">句法</span><span class="sxs-lookup"><span data-stu-id="12518-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12518-105">說明</span><span class="sxs-lookup"><span data-stu-id="12518-105">DESCRIPTION</span></span>
<span data-ttu-id="12518-106">**新的-AzureRmVmssVaultCertificateConfig** Cmdlet 會指定必須放在虛擬機器縮放集 (VMSS) 虛擬機器上的機密。</span><span class="sxs-lookup"><span data-stu-id="12518-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="12518-107">這個 Cmdlet 的輸出應該與 Add-AzureRmVmssSecret Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="12518-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="12518-108">示例</span><span class="sxs-lookup"><span data-stu-id="12518-108">EXAMPLES</span></span>

### <span data-ttu-id="12518-109">範例1：建立主要電子倉庫憑證設定</span><span class="sxs-lookup"><span data-stu-id="12518-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="12518-110">這個命令會建立一個主要的電子倉庫憑證配置，該設定會使用位於指定憑證 URL 之名為 MyCerts 的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="12518-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="12518-111">參數</span><span class="sxs-lookup"><span data-stu-id="12518-111">PARAMETERS</span></span>

### <span data-ttu-id="12518-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="12518-112">-CertificateStore</span></span>
<span data-ttu-id="12518-113">在新增憑證的規模集中，指定虛擬機器上的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="12518-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="12518-114">這僅適用于 Windows 虛擬電腦縮放集。</span><span class="sxs-lookup"><span data-stu-id="12518-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="12518-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="12518-115">-CertificateUrl</span></span>
<span data-ttu-id="12518-116">指定儲存在金鑰儲存庫中之憑證的 URI。</span><span class="sxs-lookup"><span data-stu-id="12518-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="12518-117">它是下列 JSON 物件的 base64 編碼，其編碼格式為 utf-8： {"data"： " \<Base64-encoded-certificate\> "，"資料類型"： "pfx"，"password"： " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="12518-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="12518-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12518-118">-DefaultProfile</span></span>
<span data-ttu-id="12518-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12518-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12518-120">-確認</span><span class="sxs-lookup"><span data-stu-id="12518-120">-Confirm</span></span>
<span data-ttu-id="12518-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12518-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12518-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12518-122">-WhatIf</span></span>
<span data-ttu-id="12518-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12518-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12518-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12518-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12518-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12518-125">CommonParameters</span></span>
<span data-ttu-id="12518-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12518-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12518-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12518-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12518-128">輸入</span><span class="sxs-lookup"><span data-stu-id="12518-128">INPUTS</span></span>

### <span data-ttu-id="12518-129">System.object</span><span class="sxs-lookup"><span data-stu-id="12518-129">System.String</span></span>

## <span data-ttu-id="12518-130">輸出</span><span class="sxs-lookup"><span data-stu-id="12518-130">OUTPUTS</span></span>

### <span data-ttu-id="12518-131">VaultCertificate 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="12518-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="12518-132">筆記</span><span class="sxs-lookup"><span data-stu-id="12518-132">NOTES</span></span>

## <span data-ttu-id="12518-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="12518-133">RELATED LINKS</span></span>

[<span data-ttu-id="12518-134">附加 AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="12518-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
