---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 375cc5493bd3b3cac31f4318df57e155eda918c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795566"
---
# <span data-ttu-id="45a9a-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="45a9a-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="45a9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="45a9a-103">新增憑證通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="45a9a-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="45a9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="45a9a-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45a9a-105">說明</span><span class="sxs-lookup"><span data-stu-id="45a9a-105">DESCRIPTION</span></span>
<span data-ttu-id="45a9a-106">**AzKeyVaultCertificateContact** Cmdlet 會針對 Azure 金鑰保存庫中的憑證通知新增金鑰保存庫的連絡人。</span><span class="sxs-lookup"><span data-stu-id="45a9a-106">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="45a9a-107">連絡人會收到有關事件的更新，例如憑證接近到期、證書已更新等。</span><span class="sxs-lookup"><span data-stu-id="45a9a-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="45a9a-108">這些事件是由憑證策略決定。</span><span class="sxs-lookup"><span data-stu-id="45a9a-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="45a9a-109">示例</span><span class="sxs-lookup"><span data-stu-id="45a9a-109">EXAMPLES</span></span>

### <span data-ttu-id="45a9a-110">範例1：新增主要電子倉庫憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="45a9a-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="45a9a-111">這個命令會新增 Patti，做為 ContosoKV01 金鑰電子倉庫的憑證連絡人，並傳回 **KeyVaultCertificateContact** 物件。</span><span class="sxs-lookup"><span data-stu-id="45a9a-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="45a9a-112">參數</span><span class="sxs-lookup"><span data-stu-id="45a9a-112">PARAMETERS</span></span>

### <span data-ttu-id="45a9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a9a-113">-DefaultProfile</span></span>
<span data-ttu-id="45a9a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="45a9a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a9a-115">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="45a9a-115">-EmailAddress</span></span>
<span data-ttu-id="45a9a-116">指定連絡人的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="45a9a-116">Specifies the email address of the contact.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a9a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45a9a-117">-PassThru</span></span>
<span data-ttu-id="45a9a-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="45a9a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="45a9a-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="45a9a-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a9a-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="45a9a-120">-VaultName</span></span>
<span data-ttu-id="45a9a-121">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="45a9a-121">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a9a-122">-確認</span><span class="sxs-lookup"><span data-stu-id="45a9a-122">-Confirm</span></span>
<span data-ttu-id="45a9a-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45a9a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45a9a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45a9a-124">-WhatIf</span></span>
<span data-ttu-id="45a9a-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45a9a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45a9a-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45a9a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45a9a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a9a-127">CommonParameters</span></span>
<span data-ttu-id="45a9a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45a9a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a9a-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45a9a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a9a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="45a9a-130">INPUTS</span></span>

### <span data-ttu-id="45a9a-131">所有</span><span class="sxs-lookup"><span data-stu-id="45a9a-131">None</span></span>
<span data-ttu-id="45a9a-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="45a9a-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45a9a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="45a9a-133">OUTPUTS</span></span>

### <span data-ttu-id="45a9a-134">[KeyVault] KeyVaultCertificateContact<清單></span><span class="sxs-lookup"><span data-stu-id="45a9a-134">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="45a9a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="45a9a-135">NOTES</span></span>

## <span data-ttu-id="45a9a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="45a9a-136">RELATED LINKS</span></span>

[<span data-ttu-id="45a9a-137">AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="45a9a-137">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="45a9a-138">移除-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="45a9a-138">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

