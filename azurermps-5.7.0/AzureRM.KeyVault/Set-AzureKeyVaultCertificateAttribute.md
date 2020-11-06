---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
ms.openlocfilehash: 4aac9e7079451eebda0c77ae663666fbd55dc9e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444511"
---
# <span data-ttu-id="8b610-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="8b610-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="8b610-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b610-102">SYNOPSIS</span></span>
<span data-ttu-id="8b610-103">修改憑證的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="8b610-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b610-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b610-104">SYNTAX</span></span>

### <span data-ttu-id="8b610-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="8b610-105">ByName (Default)</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b610-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b610-106">ByInputObject</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b610-107">說明</span><span class="sxs-lookup"><span data-stu-id="8b610-107">DESCRIPTION</span></span>
<span data-ttu-id="8b610-108">**AzureKeyVaultCertificateAttribute** Cmdlet 會修改憑證的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="8b610-108">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="8b610-109">示例</span><span class="sxs-lookup"><span data-stu-id="8b610-109">EXAMPLES</span></span>

### <span data-ttu-id="8b610-110">範例1：修改與憑證相關的標記</span><span class="sxs-lookup"><span data-stu-id="8b610-110">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzureKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="8b610-111">第一個命令會將一個鍵/值對陣列指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="8b610-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="8b610-112">第二個命令會將名為 TestCert01 的憑證的 [標記] 值設定為 [$Tags]。</span><span class="sxs-lookup"><span data-stu-id="8b610-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="8b610-113">最終命令會使用 Get-AzureKeyVaultCertificate Cmdlet 來驗證作業，以顯示 TestCert01 憑證。</span><span class="sxs-lookup"><span data-stu-id="8b610-113">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="8b610-114">參數</span><span class="sxs-lookup"><span data-stu-id="8b610-114">PARAMETERS</span></span>

### <span data-ttu-id="8b610-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b610-115">-DefaultProfile</span></span>
<span data-ttu-id="8b610-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8b610-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b610-117">-啟用</span><span class="sxs-lookup"><span data-stu-id="8b610-117">-Enable</span></span>
<span data-ttu-id="8b610-118">指出是否要啟用或停用憑證。</span><span class="sxs-lookup"><span data-stu-id="8b610-118">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="8b610-119">指定 $True 以啟用或 $False 來停用。</span><span class="sxs-lookup"><span data-stu-id="8b610-119">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b610-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b610-120">-InputObject</span></span>
<span data-ttu-id="8b610-121">憑證物件</span><span class="sxs-lookup"><span data-stu-id="8b610-121">Certificate object</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b610-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="8b610-122">-Name</span></span>
<span data-ttu-id="8b610-123">指定要修改的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="8b610-123">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="8b610-124">這個 Cmdlet 會根據金鑰保存庫名稱、您目前所選的環境、憑證名稱及證書版本，來構造憑證的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8b610-124">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b610-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b610-125">-PassThru</span></span>
<span data-ttu-id="8b610-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8b610-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8b610-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8b610-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8b610-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b610-128">-Tag</span></span>
<span data-ttu-id="8b610-129">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="8b610-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8b610-130">例如：</span><span class="sxs-lookup"><span data-stu-id="8b610-130">For example:</span></span>

<span data-ttu-id="8b610-131">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8b610-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b610-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8b610-132">-VaultName</span></span>
<span data-ttu-id="8b610-133">指定此 Cmdlet 修改憑證的主要保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="8b610-133">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="8b610-134">這個 Cmdlet 根據名稱和目前所選的環境來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8b610-134">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b610-135">-版本</span><span class="sxs-lookup"><span data-stu-id="8b610-135">-Version</span></span>
<span data-ttu-id="8b610-136">指定憑證版本。</span><span class="sxs-lookup"><span data-stu-id="8b610-136">Specifies the version of a certificate.</span></span>
<span data-ttu-id="8b610-137">這個 Cmdlet 會根據金鑰保存庫名稱、您目前所選的環境、憑證名稱及證書版本，來構造憑證的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8b610-137">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b610-138">-確認</span><span class="sxs-lookup"><span data-stu-id="8b610-138">-Confirm</span></span>
<span data-ttu-id="8b610-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8b610-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b610-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b610-140">-WhatIf</span></span>
<span data-ttu-id="8b610-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8b610-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b610-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b610-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b610-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b610-143">CommonParameters</span></span>
<span data-ttu-id="8b610-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b610-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b610-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b610-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b610-146">輸入</span><span class="sxs-lookup"><span data-stu-id="8b610-146">INPUTS</span></span>

### <span data-ttu-id="8b610-147">所有</span><span class="sxs-lookup"><span data-stu-id="8b610-147">None</span></span>
<span data-ttu-id="8b610-148">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8b610-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b610-149">輸出</span><span class="sxs-lookup"><span data-stu-id="8b610-149">OUTPUTS</span></span>

### <span data-ttu-id="8b610-150">PSKeyVaultCertificate 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="8b610-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="8b610-151">筆記</span><span class="sxs-lookup"><span data-stu-id="8b610-151">NOTES</span></span>

## <span data-ttu-id="8b610-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b610-152">RELATED LINKS</span></span>

[<span data-ttu-id="8b610-153">附加 AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8b610-153">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
