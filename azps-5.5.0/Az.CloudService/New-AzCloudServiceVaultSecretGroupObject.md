---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: 925d29e7d567613bbf10e88c65860ebe2ef40c2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139383"
---
# <span data-ttu-id="cc745-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="cc745-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="cc745-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc745-102">SYNOPSIS</span></span>
<span data-ttu-id="cc745-103">為保存庫密碼群組建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="cc745-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="cc745-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc745-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="cc745-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc745-105">DESCRIPTION</span></span>
<span data-ttu-id="cc745-106">針對秘密群組建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="cc745-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="cc745-107">示例</span><span class="sxs-lookup"><span data-stu-id="cc745-107">EXAMPLES</span></span>

### <span data-ttu-id="cc745-108">範例1：建立電子倉庫密碼群組物件</span><span class="sxs-lookup"><span data-stu-id="cc745-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="cc745-109">這個命令會建立用來建立或更新雲端服務的保存庫密碼群組物件。</span><span class="sxs-lookup"><span data-stu-id="cc745-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="cc745-110">如需詳細資訊，請參閱新 AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="cc745-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="cc745-111">參數</span><span class="sxs-lookup"><span data-stu-id="cc745-111">PARAMETERS</span></span>

### <span data-ttu-id="cc745-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="cc745-112">-CertificateUrl</span></span>
<span data-ttu-id="cc745-113">這是已上傳到金鑰保存庫的憑證 URL （密碼）。</span><span class="sxs-lookup"><span data-stu-id="cc745-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc745-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="cc745-114">-Id</span></span>
<span data-ttu-id="cc745-115">[主要電子倉庫資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cc745-115">Key Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc745-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc745-116">CommonParameters</span></span>
<span data-ttu-id="cc745-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc745-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc745-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cc745-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc745-119">輸入</span><span class="sxs-lookup"><span data-stu-id="cc745-119">INPUTS</span></span>

## <span data-ttu-id="cc745-120">輸出</span><span class="sxs-lookup"><span data-stu-id="cc745-120">OUTPUTS</span></span>

### <span data-ttu-id="cc745-121">CloudServiceVaultSecretGroup （CloudService）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="cc745-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="cc745-122">筆記</span><span class="sxs-lookup"><span data-stu-id="cc745-122">NOTES</span></span>

<span data-ttu-id="cc745-123">別名</span><span class="sxs-lookup"><span data-stu-id="cc745-123">ALIASES</span></span>

## <span data-ttu-id="cc745-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc745-124">RELATED LINKS</span></span>

