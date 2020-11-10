---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: f17da705ed65484e789a803308bcaddb60e409f3
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395130"
---
# <span data-ttu-id="1e637-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="1e637-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="1e637-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e637-102">SYNOPSIS</span></span>
<span data-ttu-id="1e637-103">將機密新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1e637-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="1e637-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e637-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e637-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e637-105">DESCRIPTION</span></span>
<span data-ttu-id="1e637-106">**AzVMSecret** Cmdlet 會將機密新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1e637-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="1e637-107">此值可讓您將憑證新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1e637-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="1e637-108">密碼必須儲存在金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="1e637-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="1e637-109">如需有關主要保存庫的詳細資訊，請參閱 [什麼是 Azure 金鑰保存庫？](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)。</span><span class="sxs-lookup"><span data-stu-id="1e637-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="1e637-110">如需有關 Cmdlet 的詳細資訊，請參閱 [Azure 金鑰保存庫 Cmdlet](/powershell/module/az.keyvault) 或 [AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e637-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="1e637-111">示例</span><span class="sxs-lookup"><span data-stu-id="1e637-111">EXAMPLES</span></span>

### <span data-ttu-id="1e637-112">範例1：將密碼新增至虛擬機器</span><span class="sxs-lookup"><span data-stu-id="1e637-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="1e637-113">第一個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="1e637-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1e637-114">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1e637-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="1e637-115">第二個命令會使用 Get-Credential Cmdlet 來建立認證物件，然後將結果儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="1e637-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="1e637-116">該命令會提示您輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="1e637-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="1e637-117">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="1e637-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="1e637-118">第三個命令使用 **AzVMOperatingSystem** Cmdlet 來設定儲存在 $VirtualMachine 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1e637-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="1e637-119">第四個命令會將來源電子倉庫識別碼指派給 $SourceVaultId 變數，以供日後使用。</span><span class="sxs-lookup"><span data-stu-id="1e637-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="1e637-120">此命令假設 $SubscriptionId 變數具有適當的值。</span><span class="sxs-lookup"><span data-stu-id="1e637-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="1e637-121">第五個命令會將值賦給 $CertificateStore 01 變數，以供日後使用。</span><span class="sxs-lookup"><span data-stu-id="1e637-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="1e637-122">第六個命令會指派憑證存放區的 URL。</span><span class="sxs-lookup"><span data-stu-id="1e637-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="1e637-123">第七個命令會將機密新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="1e637-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="1e637-124">SourceVaultId 參數會指定金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="1e637-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="1e637-125">此命令會指定憑證存放區的名稱和憑證的 URL。</span><span class="sxs-lookup"><span data-stu-id="1e637-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="1e637-126">您可以重複執行 **附加程式 AzVMSecret** ，以新增其他憑證的機密資訊。</span><span class="sxs-lookup"><span data-stu-id="1e637-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="1e637-127">參數</span><span class="sxs-lookup"><span data-stu-id="1e637-127">PARAMETERS</span></span>

### <span data-ttu-id="1e637-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="1e637-128">-CertificateStore</span></span>
<span data-ttu-id="1e637-129">指定執行 Windows 作業系統的虛擬機器上的憑證存放區名稱。</span><span class="sxs-lookup"><span data-stu-id="1e637-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="1e637-130">這個 Cmdlet 會將憑證新增到此參數指定的存放區。</span><span class="sxs-lookup"><span data-stu-id="1e637-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="1e637-131">您只能針對執行 Windows 作業系統的虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="1e637-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="1e637-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="1e637-132">-CertificateUrl</span></span>
<span data-ttu-id="1e637-133">指定指向包含憑證之主要 Vault 機密的 URL。</span><span class="sxs-lookup"><span data-stu-id="1e637-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="1e637-134">憑證是下列 JavaScript 物件符號的 Base64 編碼， (JSON) 物件（以 UTF-8 編碼）：</span><span class="sxs-lookup"><span data-stu-id="1e637-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="1e637-135">{"資料"： " \<Base64-encoded-file\> "，"dataType"： " \<file-format\> "，"密碼"： " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="1e637-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="1e637-136">目前，dataType 只接受 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="1e637-136">Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="1e637-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e637-137">-DefaultProfile</span></span>
<span data-ttu-id="1e637-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e637-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e637-139">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="1e637-139">-SourceVaultId</span></span>
<span data-ttu-id="1e637-140">指定包含您可以新增至虛擬機器之憑證的主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e637-140">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="1e637-141">此值也會充當新增多個憑證的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e637-141">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="1e637-142">這表示當您從相同的金鑰保存庫新增多個憑證時，可以使用與 *SourceVaultId* 相同的值。</span><span class="sxs-lookup"><span data-stu-id="1e637-142">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="1e637-143">-VM</span><span class="sxs-lookup"><span data-stu-id="1e637-143">-VM</span></span>
<span data-ttu-id="1e637-144">指定此 Cmdlet 修改的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="1e637-144">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="1e637-145">若要取得虛擬機器物件，請使用 [AzVM](./Get-AzVM.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e637-145">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="1e637-146">您可以使用 [新的 AzVMConfig](./New-AzVMConfig.md) Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="1e637-146">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="1e637-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e637-147">CommonParameters</span></span>
<span data-ttu-id="1e637-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e637-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e637-149">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e637-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e637-150">輸入</span><span class="sxs-lookup"><span data-stu-id="1e637-150">INPUTS</span></span>

### <span data-ttu-id="1e637-151">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1e637-151">PSVirtualMachine</span></span>
<span data-ttu-id="1e637-152">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="1e637-152">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="1e637-153">輸出</span><span class="sxs-lookup"><span data-stu-id="1e637-153">OUTPUTS</span></span>

### <span data-ttu-id="1e637-154">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="1e637-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1e637-155">筆記</span><span class="sxs-lookup"><span data-stu-id="1e637-155">NOTES</span></span>

## <span data-ttu-id="1e637-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e637-156">RELATED LINKS</span></span>

[<span data-ttu-id="1e637-157">AzVM</span><span class="sxs-lookup"><span data-stu-id="1e637-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1e637-158">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="1e637-158">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="1e637-159">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="1e637-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
