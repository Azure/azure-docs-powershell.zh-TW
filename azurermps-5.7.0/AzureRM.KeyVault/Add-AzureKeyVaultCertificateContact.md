---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 96f793c763a3e9a710c7e401c29880ccc0136b38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455399"
---
# <span data-ttu-id="13113-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="13113-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="13113-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13113-102">SYNOPSIS</span></span>
<span data-ttu-id="13113-103">新增憑證通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="13113-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13113-104">句法</span><span class="sxs-lookup"><span data-stu-id="13113-104">SYNTAX</span></span>

### <span data-ttu-id="13113-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="13113-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13113-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="13113-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13113-107">說明</span><span class="sxs-lookup"><span data-stu-id="13113-107">DESCRIPTION</span></span>
<span data-ttu-id="13113-108">**AzureKeyVaultCertificateContact** Cmdlet 會針對 Azure 金鑰保存庫中的憑證通知新增金鑰保存庫的連絡人。</span><span class="sxs-lookup"><span data-stu-id="13113-108">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="13113-109">連絡人會收到有關事件的更新，例如憑證接近到期、證書已更新等。</span><span class="sxs-lookup"><span data-stu-id="13113-109">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="13113-110">這些事件是由憑證策略決定。</span><span class="sxs-lookup"><span data-stu-id="13113-110">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="13113-111">示例</span><span class="sxs-lookup"><span data-stu-id="13113-111">EXAMPLES</span></span>

### <span data-ttu-id="13113-112">範例1：新增主要電子倉庫憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="13113-112">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="13113-113">這個命令會新增 Patti，做為 ContosoKV01 金鑰電子倉庫的憑證連絡人，並傳回 **KeyVaultCertificateContact** 物件。</span><span class="sxs-lookup"><span data-stu-id="13113-113">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="13113-114">參數</span><span class="sxs-lookup"><span data-stu-id="13113-114">PARAMETERS</span></span>

### <span data-ttu-id="13113-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13113-115">-DefaultProfile</span></span>
<span data-ttu-id="13113-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="13113-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13113-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="13113-117">-EmailAddress</span></span>
<span data-ttu-id="13113-118">指定連絡人的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="13113-118">Specifies the email address of the contact.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13113-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13113-119">-InputObject</span></span>
<span data-ttu-id="13113-120">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="13113-120">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13113-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13113-121">-PassThru</span></span>
<span data-ttu-id="13113-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="13113-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="13113-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="13113-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="13113-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="13113-124">-VaultName</span></span>
<span data-ttu-id="13113-125">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="13113-125">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13113-126">-確認</span><span class="sxs-lookup"><span data-stu-id="13113-126">-Confirm</span></span>
<span data-ttu-id="13113-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13113-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13113-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13113-128">-WhatIf</span></span>
<span data-ttu-id="13113-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13113-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13113-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13113-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13113-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13113-131">CommonParameters</span></span>
<span data-ttu-id="13113-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13113-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13113-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13113-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13113-134">輸入</span><span class="sxs-lookup"><span data-stu-id="13113-134">INPUTS</span></span>

### <span data-ttu-id="13113-135">所有</span><span class="sxs-lookup"><span data-stu-id="13113-135">None</span></span>
<span data-ttu-id="13113-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="13113-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="13113-137">輸出</span><span class="sxs-lookup"><span data-stu-id="13113-137">OUTPUTS</span></span>

### <span data-ttu-id="13113-138">[KeyVault] PSKeyVaultCertificateContact<清單></span><span class="sxs-lookup"><span data-stu-id="13113-138">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="13113-139">筆記</span><span class="sxs-lookup"><span data-stu-id="13113-139">NOTES</span></span>

## <span data-ttu-id="13113-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="13113-140">RELATED LINKS</span></span>

[<span data-ttu-id="13113-141">AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="13113-141">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="13113-142">移除-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="13113-142">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

