---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957092"
---
# <span data-ttu-id="124e1-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="124e1-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="124e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="124e1-102">SYNOPSIS</span></span>
<span data-ttu-id="124e1-103">新增憑證通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="124e1-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="124e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="124e1-104">SYNTAX</span></span>

### <span data-ttu-id="124e1-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="124e1-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="124e1-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="124e1-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="124e1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="124e1-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="124e1-108">說明</span><span class="sxs-lookup"><span data-stu-id="124e1-108">DESCRIPTION</span></span>
<span data-ttu-id="124e1-109">**AzKeyVaultCertificateContact** Cmdlet 會針對 Azure 金鑰保存庫中的憑證通知新增金鑰保存庫的連絡人。</span><span class="sxs-lookup"><span data-stu-id="124e1-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="124e1-110">連絡人會收到有關事件的更新，例如憑證接近到期、證書已更新等。</span><span class="sxs-lookup"><span data-stu-id="124e1-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="124e1-111">這些事件是由憑證策略決定。</span><span class="sxs-lookup"><span data-stu-id="124e1-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="124e1-112">示例</span><span class="sxs-lookup"><span data-stu-id="124e1-112">EXAMPLES</span></span>

### <span data-ttu-id="124e1-113">範例1：新增主要電子倉庫憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="124e1-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="124e1-114">這個命令會新增 Patti，做為 ContosoKV01 金鑰電子倉庫的憑證連絡人，並傳回「ContosoKV01」保存庫的連絡人清單。</span><span class="sxs-lookup"><span data-stu-id="124e1-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="124e1-115">參數</span><span class="sxs-lookup"><span data-stu-id="124e1-115">PARAMETERS</span></span>

### <span data-ttu-id="124e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="124e1-116">-DefaultProfile</span></span>
<span data-ttu-id="124e1-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="124e1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e1-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="124e1-118">-EmailAddress</span></span>
<span data-ttu-id="124e1-119">指定連絡人的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="124e1-119">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="124e1-120">-InputObject</span></span>
<span data-ttu-id="124e1-121">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="124e1-121">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="124e1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="124e1-122">-PassThru</span></span>
<span data-ttu-id="124e1-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="124e1-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="124e1-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="124e1-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="124e1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="124e1-125">-ResourceId</span></span>
<span data-ttu-id="124e1-126">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="124e1-126">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="124e1-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="124e1-127">-VaultName</span></span>
<span data-ttu-id="124e1-128">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="124e1-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e1-129">-確認</span><span class="sxs-lookup"><span data-stu-id="124e1-129">-Confirm</span></span>
<span data-ttu-id="124e1-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="124e1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="124e1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="124e1-131">-WhatIf</span></span>
<span data-ttu-id="124e1-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="124e1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="124e1-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="124e1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="124e1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="124e1-134">CommonParameters</span></span>
<span data-ttu-id="124e1-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="124e1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="124e1-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="124e1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="124e1-137">輸入</span><span class="sxs-lookup"><span data-stu-id="124e1-137">INPUTS</span></span>

### <span data-ttu-id="124e1-138">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="124e1-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="124e1-139">System.object</span><span class="sxs-lookup"><span data-stu-id="124e1-139">System.String</span></span>

## <span data-ttu-id="124e1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="124e1-140">OUTPUTS</span></span>

### <span data-ttu-id="124e1-141">PSKeyVaultCertificateContact 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="124e1-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="124e1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="124e1-142">NOTES</span></span>

## <span data-ttu-id="124e1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="124e1-143">RELATED LINKS</span></span>

[<span data-ttu-id="124e1-144">AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="124e1-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="124e1-145">移除-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="124e1-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

