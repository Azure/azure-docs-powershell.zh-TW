---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 2a79f4bb555576414b4ed14c06ee0050133e139d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456207"
---
# <span data-ttu-id="e158b-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="e158b-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="e158b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e158b-102">SYNOPSIS</span></span>
<span data-ttu-id="e158b-103">在金鑰保存庫中設定憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="e158b-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e158b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e158b-104">SYNTAX</span></span>

### <span data-ttu-id="e158b-105">展開 (預設) </span><span class="sxs-lookup"><span data-stu-id="e158b-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e158b-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="e158b-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e158b-107">說明</span><span class="sxs-lookup"><span data-stu-id="e158b-107">DESCRIPTION</span></span>
<span data-ttu-id="e158b-108">Set-AzureKeyVaultCertificateIssuer Cmdlet 會在金鑰保存庫中設定憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="e158b-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="e158b-109">示例</span><span class="sxs-lookup"><span data-stu-id="e158b-109">EXAMPLES</span></span>

### <span data-ttu-id="e158b-110">範例1：設定憑證簽發者</span><span class="sxs-lookup"><span data-stu-id="e158b-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="e158b-111">這個命令會設定憑證簽發者的屬性，然後將其儲存在 $Issuer 變數中。</span><span class="sxs-lookup"><span data-stu-id="e158b-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="e158b-112">參數</span><span class="sxs-lookup"><span data-stu-id="e158b-112">PARAMETERS</span></span>

### <span data-ttu-id="e158b-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="e158b-113">-AccountId</span></span>
<span data-ttu-id="e158b-114">指定憑證簽發者的帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="e158b-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e158b-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="e158b-115">-ApiKey</span></span>
<span data-ttu-id="e158b-116">指定憑證簽發者的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e158b-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e158b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e158b-117">-DefaultProfile</span></span>
<span data-ttu-id="e158b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e158b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e158b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e158b-119">-InputObject</span></span>
<span data-ttu-id="e158b-120">指定要設定的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="e158b-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e158b-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="e158b-121">-IssuerProvider</span></span>
<span data-ttu-id="e158b-122">指定憑證頒發者的類型。</span><span class="sxs-lookup"><span data-stu-id="e158b-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e158b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e158b-123">-Name</span></span>
<span data-ttu-id="e158b-124">指定頒發者的名稱。</span><span class="sxs-lookup"><span data-stu-id="e158b-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e158b-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="e158b-125">-OrganizationDetails</span></span>
<span data-ttu-id="e158b-126">要與頒發者搭配使用的組織詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e158b-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e158b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e158b-127">-PassThru</span></span>
<span data-ttu-id="e158b-128">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e158b-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e158b-129">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e158b-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e158b-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e158b-130">-VaultName</span></span>
<span data-ttu-id="e158b-131">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e158b-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="e158b-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e158b-132">-Confirm</span></span>
<span data-ttu-id="e158b-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e158b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e158b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e158b-134">-WhatIf</span></span>
<span data-ttu-id="e158b-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e158b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e158b-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e158b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e158b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e158b-137">CommonParameters</span></span>
<span data-ttu-id="e158b-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e158b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e158b-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e158b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e158b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e158b-140">INPUTS</span></span>

### <span data-ttu-id="e158b-141">所有</span><span class="sxs-lookup"><span data-stu-id="e158b-141">None</span></span>
<span data-ttu-id="e158b-142">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e158b-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e158b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e158b-143">OUTPUTS</span></span>

### <span data-ttu-id="e158b-144">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e158b-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="e158b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e158b-145">NOTES</span></span>

## <span data-ttu-id="e158b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e158b-146">RELATED LINKS</span></span>

[<span data-ttu-id="e158b-147">AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="e158b-147">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="e158b-148">移除-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="e158b-148">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

