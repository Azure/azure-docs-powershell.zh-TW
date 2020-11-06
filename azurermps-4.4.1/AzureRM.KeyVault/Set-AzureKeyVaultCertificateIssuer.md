---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: eac75ae5c9828493244ace01b6c090fda7e6ef5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451667"
---
# <span data-ttu-id="0f0cb-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0f0cb-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="0f0cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f0cb-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0cb-103">在金鑰保存庫中設定憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f0cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f0cb-104">SYNTAX</span></span>

### <span data-ttu-id="0f0cb-105">展開 (預設) </span><span class="sxs-lookup"><span data-stu-id="0f0cb-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f0cb-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="0f0cb-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f0cb-107">說明</span><span class="sxs-lookup"><span data-stu-id="0f0cb-107">DESCRIPTION</span></span>
<span data-ttu-id="0f0cb-108">Set-AzureKeyVaultCertificateIssuer Cmdlet 會在金鑰保存庫中設定憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="0f0cb-109">示例</span><span class="sxs-lookup"><span data-stu-id="0f0cb-109">EXAMPLES</span></span>

### <span data-ttu-id="0f0cb-110">範例1：設定憑證簽發者</span><span class="sxs-lookup"><span data-stu-id="0f0cb-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="0f0cb-111">這個命令會設定憑證簽發者的屬性，然後將其儲存在 $Issuer 變數中。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="0f0cb-112">參數</span><span class="sxs-lookup"><span data-stu-id="0f0cb-112">PARAMETERS</span></span>

### <span data-ttu-id="0f0cb-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="0f0cb-113">-AccountId</span></span>
<span data-ttu-id="0f0cb-114">指定憑證簽發者的帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0cb-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="0f0cb-115">-ApiKey</span></span>
<span data-ttu-id="0f0cb-116">指定憑證簽發者的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0cb-117">-Issuer</span><span class="sxs-lookup"><span data-stu-id="0f0cb-117">-Issuer</span></span>
<span data-ttu-id="0f0cb-118">指定要更新的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-118">Specifies the certificate issuer to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0cb-119">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="0f0cb-119">-IssuerProvider</span></span>
<span data-ttu-id="0f0cb-120">指定憑證頒發者的類型。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-120">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0cb-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f0cb-121">-Name</span></span>
<span data-ttu-id="0f0cb-122">指定頒發者的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-122">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0cb-123">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="0f0cb-123">-OrganizationDetails</span></span>
<span data-ttu-id="0f0cb-124">要與頒發者搭配使用的組織詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-124">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0cb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f0cb-125">-PassThru</span></span>
<span data-ttu-id="0f0cb-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f0cb-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f0cb-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0f0cb-128">-VaultName</span></span>
<span data-ttu-id="0f0cb-129">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-129">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="0f0cb-130">-確認</span><span class="sxs-lookup"><span data-stu-id="0f0cb-130">-Confirm</span></span>
<span data-ttu-id="0f0cb-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f0cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f0cb-132">-WhatIf</span></span>
<span data-ttu-id="0f0cb-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f0cb-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f0cb-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0cb-135">-DefaultProfile</span></span>
<span data-ttu-id="0f0cb-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f0cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0cb-137">CommonParameters</span></span>
<span data-ttu-id="0f0cb-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0cb-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0cb-140">輸入</span><span class="sxs-lookup"><span data-stu-id="0f0cb-140">INPUTS</span></span>

## <span data-ttu-id="0f0cb-141">輸出</span><span class="sxs-lookup"><span data-stu-id="0f0cb-141">OUTPUTS</span></span>

### <span data-ttu-id="0f0cb-142">KeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="0f0cb-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0f0cb-143">筆記</span><span class="sxs-lookup"><span data-stu-id="0f0cb-143">NOTES</span></span>

## <span data-ttu-id="0f0cb-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f0cb-144">RELATED LINKS</span></span>

[<span data-ttu-id="0f0cb-145">AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0f0cb-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="0f0cb-146">移除-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0f0cb-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

