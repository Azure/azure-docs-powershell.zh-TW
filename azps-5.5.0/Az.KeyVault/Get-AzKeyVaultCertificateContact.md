---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133110"
---
# <span data-ttu-id="7b175-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7b175-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="7b175-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b175-102">SYNOPSIS</span></span>
<span data-ttu-id="7b175-103">取得針對金鑰保存庫的憑證通知所註冊的連絡人。</span><span class="sxs-lookup"><span data-stu-id="7b175-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="7b175-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b175-104">SYNTAX</span></span>

### <span data-ttu-id="7b175-105">VaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="7b175-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b175-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7b175-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b175-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b175-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b175-108">說明</span><span class="sxs-lookup"><span data-stu-id="7b175-108">DESCRIPTION</span></span>
<span data-ttu-id="7b175-109">**AzKeyVaultCertificateContact** Cmdlet 會取得已針對 Azure 金鑰保存庫中的金鑰電子倉庫的憑證通知登錄的連絡人。</span><span class="sxs-lookup"><span data-stu-id="7b175-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="7b175-110">示例</span><span class="sxs-lookup"><span data-stu-id="7b175-110">EXAMPLES</span></span>

### <span data-ttu-id="7b175-111">範例1：取得所有憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="7b175-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="7b175-112">這個命令會在 Contoso [主要電子倉庫] 中取得證書物件的所有連絡人，然後將它們儲存在 $Contacts 變數中。</span><span class="sxs-lookup"><span data-stu-id="7b175-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="7b175-113">參數</span><span class="sxs-lookup"><span data-stu-id="7b175-113">PARAMETERS</span></span>

### <span data-ttu-id="7b175-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b175-114">-DefaultProfile</span></span>
<span data-ttu-id="7b175-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7b175-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b175-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b175-116">-InputObject</span></span>
<span data-ttu-id="7b175-117">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="7b175-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b175-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b175-118">-ResourceId</span></span>
<span data-ttu-id="7b175-119">KeyVault Id。</span><span class="sxs-lookup"><span data-stu-id="7b175-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="7b175-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7b175-120">-VaultName</span></span>
<span data-ttu-id="7b175-121">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b175-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b175-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b175-122">CommonParameters</span></span>
<span data-ttu-id="7b175-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b175-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b175-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7b175-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b175-125">輸入</span><span class="sxs-lookup"><span data-stu-id="7b175-125">INPUTS</span></span>

### <span data-ttu-id="7b175-126">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="7b175-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="7b175-127">System.object</span><span class="sxs-lookup"><span data-stu-id="7b175-127">System.String</span></span>

## <span data-ttu-id="7b175-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7b175-128">OUTPUTS</span></span>

### <span data-ttu-id="7b175-129">PSKeyVaultCertificateContact 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="7b175-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="7b175-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7b175-130">NOTES</span></span>

## <span data-ttu-id="7b175-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b175-131">RELATED LINKS</span></span>

[<span data-ttu-id="7b175-132">附加 AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7b175-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="7b175-133">移除-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7b175-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

