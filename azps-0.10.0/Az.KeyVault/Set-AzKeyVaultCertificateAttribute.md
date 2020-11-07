---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
ms.openlocfilehash: 9297e523e623542c19df1915d3da29d9e39cec40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795531"
---
# <span data-ttu-id="8af03-101">Set-AzKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="8af03-101">Set-AzKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="8af03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8af03-102">SYNOPSIS</span></span>
<span data-ttu-id="8af03-103">修改憑證的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="8af03-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="8af03-104">句法</span><span class="sxs-lookup"><span data-stu-id="8af03-104">SYNTAX</span></span>

```
Set-AzKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af03-105">說明</span><span class="sxs-lookup"><span data-stu-id="8af03-105">DESCRIPTION</span></span>
<span data-ttu-id="8af03-106">**AzKeyVaultCertificateAttribute** Cmdlet 會修改憑證的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="8af03-106">The **Set-AzKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="8af03-107">示例</span><span class="sxs-lookup"><span data-stu-id="8af03-107">EXAMPLES</span></span>

### <span data-ttu-id="8af03-108">範例1：修改與憑證相關的標記</span><span class="sxs-lookup"><span data-stu-id="8af03-108">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="8af03-109">第一個命令會將一個鍵/值對陣列指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="8af03-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="8af03-110">第二個命令會將名為 TestCert01 的憑證的 [標記] 值設定為 [$Tags]。</span><span class="sxs-lookup"><span data-stu-id="8af03-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="8af03-111">最終命令會使用 Get-AzKeyVaultCertificate Cmdlet 來驗證作業，以顯示 TestCert01 憑證。</span><span class="sxs-lookup"><span data-stu-id="8af03-111">The final command displays the TestCert01 certificate by using the Get-AzKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="8af03-112">參數</span><span class="sxs-lookup"><span data-stu-id="8af03-112">PARAMETERS</span></span>

### <span data-ttu-id="8af03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af03-113">-DefaultProfile</span></span>
<span data-ttu-id="8af03-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8af03-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8af03-115">-啟用</span><span class="sxs-lookup"><span data-stu-id="8af03-115">-Enable</span></span>
<span data-ttu-id="8af03-116">指出是否要啟用或停用憑證。</span><span class="sxs-lookup"><span data-stu-id="8af03-116">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="8af03-117">指定 $True 以啟用或 $False 來停用。</span><span class="sxs-lookup"><span data-stu-id="8af03-117">Specify $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="8af03-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8af03-118">-Name</span></span>
<span data-ttu-id="8af03-119">指定要修改的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="8af03-119">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="8af03-120">這個 Cmdlet 會根據金鑰保存庫名稱、您目前所選的環境、憑證名稱及證書版本，來構造憑證的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8af03-120">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af03-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8af03-121">-PassThru</span></span>
<span data-ttu-id="8af03-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8af03-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8af03-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8af03-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8af03-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="8af03-124">-Tag</span></span>
<span data-ttu-id="8af03-125">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="8af03-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8af03-126">例如：</span><span class="sxs-lookup"><span data-stu-id="8af03-126">For example:</span></span>

<span data-ttu-id="8af03-127">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8af03-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8af03-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8af03-128">-VaultName</span></span>
<span data-ttu-id="8af03-129">指定此 Cmdlet 修改憑證的主要保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="8af03-129">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="8af03-130">這個 Cmdlet 根據名稱和目前所選的環境來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8af03-130">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8af03-131">-版本</span><span class="sxs-lookup"><span data-stu-id="8af03-131">-Version</span></span>
<span data-ttu-id="8af03-132">指定憑證版本。</span><span class="sxs-lookup"><span data-stu-id="8af03-132">Specifies the version of a certificate.</span></span>
<span data-ttu-id="8af03-133">這個 Cmdlet 會根據金鑰保存庫名稱、您目前所選的環境、憑證名稱及證書版本，來構造憑證的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8af03-133">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

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

### <span data-ttu-id="8af03-134">-確認</span><span class="sxs-lookup"><span data-stu-id="8af03-134">-Confirm</span></span>
<span data-ttu-id="8af03-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8af03-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af03-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af03-136">-WhatIf</span></span>
<span data-ttu-id="8af03-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8af03-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af03-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8af03-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af03-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af03-139">CommonParameters</span></span>
<span data-ttu-id="8af03-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8af03-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af03-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8af03-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af03-142">輸入</span><span class="sxs-lookup"><span data-stu-id="8af03-142">INPUTS</span></span>

### <span data-ttu-id="8af03-143">所有</span><span class="sxs-lookup"><span data-stu-id="8af03-143">None</span></span>
<span data-ttu-id="8af03-144">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8af03-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8af03-145">輸出</span><span class="sxs-lookup"><span data-stu-id="8af03-145">OUTPUTS</span></span>

### <span data-ttu-id="8af03-146">KeyVaultCertificate 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="8af03-146">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="8af03-147">筆記</span><span class="sxs-lookup"><span data-stu-id="8af03-147">NOTES</span></span>

## <span data-ttu-id="8af03-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="8af03-148">RELATED LINKS</span></span>

[<span data-ttu-id="8af03-149">附加 AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8af03-149">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)
