---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
ms.openlocfilehash: 517614e93510aab163f5d632705e4a5a3566186a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448761"
---
# <span data-ttu-id="4a3f7-101">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="4a3f7-101">Add-AzureRmVMSecret</span></span>

## <span data-ttu-id="4a3f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3f7-103">將機密新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-103">Adds a secret to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a3f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a3f7-104">SYNTAX</span></span>

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [<CommonParameters>]
```

## <span data-ttu-id="4a3f7-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a3f7-105">DESCRIPTION</span></span>
<span data-ttu-id="4a3f7-106">**AzureRmVMSecret** Cmdlet 會將機密新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-106">The **Add-AzureRmVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="4a3f7-107">此值可讓您將憑證新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="4a3f7-108">密碼必須儲存在金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="4a3f7-109">如需有關主要保存庫的詳細資訊，請參閱 [什麼是 Azure 金鑰保存庫？](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="4a3f7-110">如需有關 Cmdlet 的詳細資訊，請參閱 Microsoft 開發人員網路庫或[AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) Cmdlet 中的[Azure 金鑰保存庫 Cmdlet](https://msdn.microsoft.com/library/azure/dn868052.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="4a3f7-111">示例</span><span class="sxs-lookup"><span data-stu-id="4a3f7-111">EXAMPLES</span></span>

### <span data-ttu-id="4a3f7-112">範例1：將密碼新增至虛擬機器</span><span class="sxs-lookup"><span data-stu-id="4a3f7-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="4a3f7-113">第一個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4a3f7-114">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="4a3f7-115">第二個命令會使用 Get-Credential Cmdlet 來建立認證物件，然後將結果儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="4a3f7-116">該命令會提示您輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="4a3f7-117">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="4a3f7-118">第三個命令使用 **AzureRmVMOperatingSystem** Cmdlet 來設定儲存在 $VirtualMachine 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-118">The third command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="4a3f7-119">第四個命令會將來源電子倉庫識別碼指派給 $SourceVaultId 變數，以供日後使用。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="4a3f7-120">此命令假設 $SubscriptionId 變數具有適當的值。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="4a3f7-121">第五個命令會將值賦給 $CertificateStore 01 變數，以供日後使用。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="4a3f7-122">第六個命令會指派憑證存放區的 URL。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="4a3f7-123">第七個命令會將機密新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4a3f7-124">SourceVaultId 參數會指定金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="4a3f7-125">此命令會指定憑證存放區的名稱和憑證的 URL。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="4a3f7-126">您可以重複執行 **附加程式 AzureRmVMSecret** ，以新增其他憑證的機密資訊。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-126">You can run the **Add-AzureRmVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="4a3f7-127">參數</span><span class="sxs-lookup"><span data-stu-id="4a3f7-127">PARAMETERS</span></span>

### <span data-ttu-id="4a3f7-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="4a3f7-128">-CertificateStore</span></span>
<span data-ttu-id="4a3f7-129">指定執行 Windows 作業系統的虛擬機器上的憑證存放區名稱。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="4a3f7-130">這個 Cmdlet 會將憑證新增到此參數指定的存放區。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="4a3f7-131">您只能針對執行 Windows 作業系統的虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3f7-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="4a3f7-132">-CertificateUrl</span></span>
<span data-ttu-id="4a3f7-133">指定指向包含憑證之主要 Vault 機密的 URL。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="4a3f7-134">憑證是下列 JavaScript 物件符號的 Base64 編碼， (JSON) 物件（以 UTF-8 編碼）：</span><span class="sxs-lookup"><span data-stu-id="4a3f7-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="4a3f7-135">{"資料"： " \<Base64-encoded-file\> "，"dataType"： " \<file-format\> "，"密碼"： " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="4a3f7-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="4a3f7-136">目前，dataType 只接受 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-136">Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3f7-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4a3f7-137">-SourceVaultId</span></span>
<span data-ttu-id="4a3f7-138">指定包含您可以新增至虛擬機器之憑證的主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="4a3f7-139">此值也會充當新增多個憑證的金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="4a3f7-140">這表示當您從相同的金鑰保存庫新增多個憑證時，可以使用與 *SourceVaultId* 相同的值。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3f7-141">-VM</span><span class="sxs-lookup"><span data-stu-id="4a3f7-141">-VM</span></span>
<span data-ttu-id="4a3f7-142">指定此 Cmdlet 修改的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="4a3f7-143">若要取得虛擬機器物件，請使用 [AzureRmVM](./Get-AzureRmVM.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-143">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="4a3f7-144">您可以使用 [新的 AzureRmVMConfig](./New-AzureRmVMConfig.md) Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-144">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3f7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3f7-145">CommonParameters</span></span>
<span data-ttu-id="4a3f7-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3f7-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3f7-148">輸入</span><span class="sxs-lookup"><span data-stu-id="4a3f7-148">INPUTS</span></span>

### <span data-ttu-id="4a3f7-149">所有</span><span class="sxs-lookup"><span data-stu-id="4a3f7-149">None</span></span>
<span data-ttu-id="4a3f7-150">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4a3f7-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4a3f7-151">輸出</span><span class="sxs-lookup"><span data-stu-id="4a3f7-151">OUTPUTS</span></span>

## <span data-ttu-id="4a3f7-152">筆記</span><span class="sxs-lookup"><span data-stu-id="4a3f7-152">NOTES</span></span>

## <span data-ttu-id="4a3f7-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a3f7-153">RELATED LINKS</span></span>

[<span data-ttu-id="4a3f7-154">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4a3f7-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="4a3f7-155">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="4a3f7-155">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="4a3f7-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4a3f7-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)
