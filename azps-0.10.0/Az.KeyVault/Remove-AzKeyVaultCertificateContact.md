---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 0b92fcb3725d42ac7c2978600f7903d6bf7f6142
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794661"
---
# <span data-ttu-id="054fb-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="054fb-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="054fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="054fb-102">SYNOPSIS</span></span>
<span data-ttu-id="054fb-103">從金鑰保存庫刪除已登錄到證書通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="054fb-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="054fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="054fb-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="054fb-105">說明</span><span class="sxs-lookup"><span data-stu-id="054fb-105">DESCRIPTION</span></span>
<span data-ttu-id="054fb-106">**AzKeyVaultCertificateContact** Cmdlet 會從金鑰保存庫中刪除已登錄到證書通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="054fb-106">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="054fb-107">示例</span><span class="sxs-lookup"><span data-stu-id="054fb-107">EXAMPLES</span></span>

### <span data-ttu-id="054fb-108">範例1：移除憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="054fb-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="054fb-109">這個命令會以 Contoso01 金鑰電子倉庫的憑證連絡人的身分移除 Patti 更完整的資訊。</span><span class="sxs-lookup"><span data-stu-id="054fb-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="054fb-110">參數</span><span class="sxs-lookup"><span data-stu-id="054fb-110">PARAMETERS</span></span>

### <span data-ttu-id="054fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="054fb-111">-DefaultProfile</span></span>
<span data-ttu-id="054fb-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="054fb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="054fb-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="054fb-113">-EmailAddress</span></span>
<span data-ttu-id="054fb-114">指定要移除之連絡人的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="054fb-114">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="054fb-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="054fb-115">-PassThru</span></span>
<span data-ttu-id="054fb-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="054fb-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="054fb-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="054fb-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="054fb-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="054fb-118">-VaultName</span></span>
<span data-ttu-id="054fb-119">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="054fb-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="054fb-120">-確認</span><span class="sxs-lookup"><span data-stu-id="054fb-120">-Confirm</span></span>
<span data-ttu-id="054fb-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="054fb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="054fb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="054fb-122">-WhatIf</span></span>
<span data-ttu-id="054fb-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="054fb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="054fb-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="054fb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="054fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="054fb-125">CommonParameters</span></span>
<span data-ttu-id="054fb-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="054fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="054fb-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="054fb-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="054fb-128">輸入</span><span class="sxs-lookup"><span data-stu-id="054fb-128">INPUTS</span></span>

### <span data-ttu-id="054fb-129">所有</span><span class="sxs-lookup"><span data-stu-id="054fb-129">None</span></span>
<span data-ttu-id="054fb-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="054fb-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="054fb-131">輸出</span><span class="sxs-lookup"><span data-stu-id="054fb-131">OUTPUTS</span></span>

### <span data-ttu-id="054fb-132">[System.object]. 清單 ' 1 [KeyVault]。 KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="054fb-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="054fb-133">筆記</span><span class="sxs-lookup"><span data-stu-id="054fb-133">NOTES</span></span>

## <span data-ttu-id="054fb-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="054fb-134">RELATED LINKS</span></span>

[<span data-ttu-id="054fb-135">附加 AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="054fb-135">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="054fb-136">AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="054fb-136">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

