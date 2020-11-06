---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: af66ad82d37c29d1dcd455cb3ccf7ae11676828c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455771"
---
# <span data-ttu-id="9c225-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9c225-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="9c225-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c225-102">SYNOPSIS</span></span>
<span data-ttu-id="9c225-103">新增憑證通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="9c225-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c225-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c225-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c225-105">說明</span><span class="sxs-lookup"><span data-stu-id="9c225-105">DESCRIPTION</span></span>
<span data-ttu-id="9c225-106">**AzureKeyVaultCertificateContact** Cmdlet 會針對 Azure 金鑰保存庫中的憑證通知新增金鑰保存庫的連絡人。</span><span class="sxs-lookup"><span data-stu-id="9c225-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="9c225-107">連絡人會收到有關事件的更新，例如憑證接近到期、證書已更新等。</span><span class="sxs-lookup"><span data-stu-id="9c225-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="9c225-108">這些事件是由憑證策略決定。</span><span class="sxs-lookup"><span data-stu-id="9c225-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="9c225-109">示例</span><span class="sxs-lookup"><span data-stu-id="9c225-109">EXAMPLES</span></span>

### <span data-ttu-id="9c225-110">範例1：新增主要電子倉庫憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="9c225-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="9c225-111">這個命令會新增 Patti，做為 ContosoKV01 金鑰電子倉庫的憑證連絡人，並傳回 **KeyVaultCertificateContact** 物件。</span><span class="sxs-lookup"><span data-stu-id="9c225-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="9c225-112">參數</span><span class="sxs-lookup"><span data-stu-id="9c225-112">PARAMETERS</span></span>

### <span data-ttu-id="9c225-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="9c225-113">-EmailAddress</span></span>
<span data-ttu-id="9c225-114">指定連絡人的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="9c225-114">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c225-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c225-115">-PassThru</span></span>
<span data-ttu-id="9c225-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="9c225-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9c225-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="9c225-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c225-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9c225-118">-VaultName</span></span>
<span data-ttu-id="9c225-119">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c225-119">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c225-120">-確認</span><span class="sxs-lookup"><span data-stu-id="9c225-120">-Confirm</span></span>
<span data-ttu-id="9c225-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c225-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c225-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c225-122">-WhatIf</span></span>
<span data-ttu-id="9c225-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c225-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c225-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c225-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c225-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c225-125">-DefaultProfile</span></span>
<span data-ttu-id="9c225-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c225-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c225-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c225-127">CommonParameters</span></span>
<span data-ttu-id="9c225-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c225-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c225-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c225-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c225-130">輸入</span><span class="sxs-lookup"><span data-stu-id="9c225-130">INPUTS</span></span>

## <span data-ttu-id="9c225-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9c225-131">OUTPUTS</span></span>

### <span data-ttu-id="9c225-132">[KeyVault] KeyVaultCertificateContact<清單></span><span class="sxs-lookup"><span data-stu-id="9c225-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="9c225-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9c225-133">NOTES</span></span>

## <span data-ttu-id="9c225-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c225-134">RELATED LINKS</span></span>

[<span data-ttu-id="9c225-135">AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9c225-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="9c225-136">移除-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9c225-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

