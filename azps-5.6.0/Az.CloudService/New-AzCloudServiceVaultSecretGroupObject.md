---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: f4d45cddd893ece419fab38759425bb104b64522
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912906"
---
# <span data-ttu-id="785b4-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="785b4-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="785b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="785b4-102">SYNOPSIS</span></span>
<span data-ttu-id="785b4-103">為 Vault 機密群組建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="785b4-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="785b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="785b4-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="785b4-105">描述</span><span class="sxs-lookup"><span data-stu-id="785b4-105">DESCRIPTION</span></span>
<span data-ttu-id="785b4-106">為機密群組建立記憶體中的物件</span><span class="sxs-lookup"><span data-stu-id="785b4-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="785b4-107">例子</span><span class="sxs-lookup"><span data-stu-id="785b4-107">EXAMPLES</span></span>

### <span data-ttu-id="785b4-108">範例 1：建立 Vault 機密群組物件</span><span class="sxs-lookup"><span data-stu-id="785b4-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="785b4-109">此命令會建立用於建立或更新雲端服務的庫機密群組物件。</span><span class="sxs-lookup"><span data-stu-id="785b4-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="785b4-110">詳情請參閱 New-AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="785b4-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="785b4-111">參數</span><span class="sxs-lookup"><span data-stu-id="785b4-111">PARAMETERS</span></span>

### <span data-ttu-id="785b4-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="785b4-112">-CertificateUrl</span></span>
<span data-ttu-id="785b4-113">這是憑證的 URL，已上傳至金鑰庫作為機密。</span><span class="sxs-lookup"><span data-stu-id="785b4-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

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

### <span data-ttu-id="785b4-114">-Id</span><span class="sxs-lookup"><span data-stu-id="785b4-114">-Id</span></span>
<span data-ttu-id="785b4-115">Key Vault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="785b4-115">Key Vault Resource Id.</span></span>

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

### <span data-ttu-id="785b4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785b4-116">CommonParameters</span></span>
<span data-ttu-id="785b4-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="785b4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785b4-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="785b4-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785b4-119">輸入</span><span class="sxs-lookup"><span data-stu-id="785b4-119">INPUTS</span></span>

## <span data-ttu-id="785b4-120">輸出</span><span class="sxs-lookup"><span data-stu-id="785b4-120">OUTPUTS</span></span>

### <span data-ttu-id="785b4-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.CloudServiceVaultSecretGroup</span><span class="sxs-lookup"><span data-stu-id="785b4-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="785b4-122">筆記</span><span class="sxs-lookup"><span data-stu-id="785b4-122">NOTES</span></span>

<span data-ttu-id="785b4-123">別名</span><span class="sxs-lookup"><span data-stu-id="785b4-123">ALIASES</span></span>

## <span data-ttu-id="785b4-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="785b4-124">RELATED LINKS</span></span>

