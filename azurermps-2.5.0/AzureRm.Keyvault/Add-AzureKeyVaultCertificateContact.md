---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: 9f52889f044ba6bf497b57a53f3e2daaea0dbf3b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799909"
---
# <span data-ttu-id="615e5-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="615e5-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="615e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="615e5-102">SYNOPSIS</span></span>
<span data-ttu-id="615e5-103">新增憑證通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="615e5-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="615e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="615e5-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="615e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="615e5-105">DESCRIPTION</span></span>
<span data-ttu-id="615e5-106">**AzureKeyVaultCertificateContact** Cmdlet 會針對 Azure 金鑰保存庫中的憑證通知新增金鑰保存庫的連絡人。</span><span class="sxs-lookup"><span data-stu-id="615e5-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="615e5-107">連絡人會收到有關事件的更新，例如憑證接近到期、證書已更新等。</span><span class="sxs-lookup"><span data-stu-id="615e5-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="615e5-108">這些事件是由憑證策略決定。</span><span class="sxs-lookup"><span data-stu-id="615e5-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="615e5-109">示例</span><span class="sxs-lookup"><span data-stu-id="615e5-109">EXAMPLES</span></span>

### <span data-ttu-id="615e5-110">範例1：新增主要電子倉庫憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="615e5-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="615e5-111">這個命令會新增 Patti，做為 ContosoKV01 金鑰電子倉庫的憑證連絡人，並傳回 **KeyVaultCertificateContact** 物件。</span><span class="sxs-lookup"><span data-stu-id="615e5-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="615e5-112">參數</span><span class="sxs-lookup"><span data-stu-id="615e5-112">PARAMETERS</span></span>

### <span data-ttu-id="615e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="615e5-113">-DefaultProfile</span></span>
<span data-ttu-id="615e5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="615e5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="615e5-115">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="615e5-115">-EmailAddress</span></span>
<span data-ttu-id="615e5-116">指定連絡人的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="615e5-116">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="615e5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="615e5-117">-PassThru</span></span>
<span data-ttu-id="615e5-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="615e5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="615e5-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="615e5-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="615e5-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="615e5-120">-VaultName</span></span>
<span data-ttu-id="615e5-121">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="615e5-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="615e5-122">-確認</span><span class="sxs-lookup"><span data-stu-id="615e5-122">-Confirm</span></span>
<span data-ttu-id="615e5-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="615e5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="615e5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="615e5-124">-WhatIf</span></span>
<span data-ttu-id="615e5-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="615e5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="615e5-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="615e5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="615e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="615e5-127">CommonParameters</span></span>
<span data-ttu-id="615e5-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="615e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="615e5-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="615e5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="615e5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="615e5-130">INPUTS</span></span>

## <span data-ttu-id="615e5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="615e5-131">OUTPUTS</span></span>

### <span data-ttu-id="615e5-132">[KeyVault] KeyVaultCertificateContact<清單></span><span class="sxs-lookup"><span data-stu-id="615e5-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="615e5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="615e5-133">NOTES</span></span>

## <span data-ttu-id="615e5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="615e5-134">RELATED LINKS</span></span>

[<span data-ttu-id="615e5-135">AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="615e5-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="615e5-136">移除-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="615e5-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

