---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 5dd9b4f8dded86a0a900a3bb3942b633c29f7020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455860"
---
# <span data-ttu-id="67efb-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="67efb-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="67efb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67efb-102">SYNOPSIS</span></span>
<span data-ttu-id="67efb-103">建立金鑰 Vault 憑證設定。</span><span class="sxs-lookup"><span data-stu-id="67efb-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67efb-104">句法</span><span class="sxs-lookup"><span data-stu-id="67efb-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67efb-105">說明</span><span class="sxs-lookup"><span data-stu-id="67efb-105">DESCRIPTION</span></span>
<span data-ttu-id="67efb-106">**新的-AzureRmVmssVaultCertificateConfig** Cmdlet 會指定必須放在虛擬機器縮放集 (VMSS) 虛擬機器上的機密。</span><span class="sxs-lookup"><span data-stu-id="67efb-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="67efb-107">這個 Cmdlet 的輸出應該與 Add-AzureRmVmssSecret Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="67efb-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="67efb-108">示例</span><span class="sxs-lookup"><span data-stu-id="67efb-108">EXAMPLES</span></span>

### <span data-ttu-id="67efb-109">範例1：建立主要電子倉庫憑證設定</span><span class="sxs-lookup"><span data-stu-id="67efb-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="67efb-110">這個命令會建立一個主要的電子倉庫憑證配置，該設定會使用位於指定憑證 URL 之名為 MyCerts 的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="67efb-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="67efb-111">參數</span><span class="sxs-lookup"><span data-stu-id="67efb-111">PARAMETERS</span></span>

### <span data-ttu-id="67efb-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="67efb-112">-CertificateStore</span></span>
<span data-ttu-id="67efb-113">在新增憑證的規模集中，指定虛擬機器上的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="67efb-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="67efb-114">這僅適用于 Windows 虛擬電腦縮放集。</span><span class="sxs-lookup"><span data-stu-id="67efb-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="67efb-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="67efb-115">-CertificateUrl</span></span>
<span data-ttu-id="67efb-116">指定儲存在金鑰儲存庫中之憑證的 URI。</span><span class="sxs-lookup"><span data-stu-id="67efb-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="67efb-117">它是以 UTF-8 編碼的下列 JSON 物件的 base64 編碼：</span><span class="sxs-lookup"><span data-stu-id="67efb-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="67efb-118">{"data"： " \<Base64-encoded-certificate\> "，"資料類型"： "pfx"，"password"： " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="67efb-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="67efb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67efb-119">-DefaultProfile</span></span>
<span data-ttu-id="67efb-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67efb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67efb-121">-確認</span><span class="sxs-lookup"><span data-stu-id="67efb-121">-Confirm</span></span>
<span data-ttu-id="67efb-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67efb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67efb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67efb-123">-WhatIf</span></span>
<span data-ttu-id="67efb-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67efb-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67efb-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67efb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67efb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67efb-126">CommonParameters</span></span>
<span data-ttu-id="67efb-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67efb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67efb-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67efb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67efb-129">輸入</span><span class="sxs-lookup"><span data-stu-id="67efb-129">INPUTS</span></span>

## <span data-ttu-id="67efb-130">輸出</span><span class="sxs-lookup"><span data-stu-id="67efb-130">OUTPUTS</span></span>

###  
<span data-ttu-id="67efb-131">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="67efb-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="67efb-132">筆記</span><span class="sxs-lookup"><span data-stu-id="67efb-132">NOTES</span></span>

## <span data-ttu-id="67efb-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="67efb-133">RELATED LINKS</span></span>

[<span data-ttu-id="67efb-134">附加 AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="67efb-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
