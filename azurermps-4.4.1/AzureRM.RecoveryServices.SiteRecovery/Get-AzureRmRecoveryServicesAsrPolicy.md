---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7ac4db45f9eb0332217c5097802904cd2146aca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456447"
---
# <span data-ttu-id="0baf4-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0baf4-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="0baf4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0baf4-102">SYNOPSIS</span></span>
<span data-ttu-id="0baf4-103">取得 ASR 複製原則。</span><span class="sxs-lookup"><span data-stu-id="0baf4-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0baf4-104">句法</span><span class="sxs-lookup"><span data-stu-id="0baf4-104">SYNTAX</span></span>

### <span data-ttu-id="0baf4-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="0baf4-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [<CommonParameters>]
```

### <span data-ttu-id="0baf4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0baf4-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="0baf4-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0baf4-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="0baf4-108">說明</span><span class="sxs-lookup"><span data-stu-id="0baf4-108">DESCRIPTION</span></span>
<span data-ttu-id="0baf4-109">AzureRmRecoveryServicesAsrPolicy Cmdlet 會透過名稱 **取得** 已設定的 Azure 網站復原複製原則或特定複製原則的清單。</span><span class="sxs-lookup"><span data-stu-id="0baf4-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="0baf4-110">示例</span><span class="sxs-lookup"><span data-stu-id="0baf4-110">EXAMPLES</span></span>

### <span data-ttu-id="0baf4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0baf4-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy -Name $PolicyName
```

<span data-ttu-id="0baf4-112">Retruns 具有指定名稱的複製原則。</span><span class="sxs-lookup"><span data-stu-id="0baf4-112">Retruns the replication policy with the specified name.</span></span>

## <span data-ttu-id="0baf4-113">參數</span><span class="sxs-lookup"><span data-stu-id="0baf4-113">PARAMETERS</span></span>

### <span data-ttu-id="0baf4-114">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0baf4-114">-FriendlyName</span></span>
<span data-ttu-id="0baf4-115">指定 ASR 複製原則的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="0baf4-115">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0baf4-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="0baf4-116">-Name</span></span>
<span data-ttu-id="0baf4-117">指定 ASR 複製原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="0baf4-117">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0baf4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0baf4-118">CommonParameters</span></span>
<span data-ttu-id="0baf4-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0baf4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0baf4-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0baf4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0baf4-121">輸入</span><span class="sxs-lookup"><span data-stu-id="0baf4-121">INPUTS</span></span>

### <span data-ttu-id="0baf4-122">所有</span><span class="sxs-lookup"><span data-stu-id="0baf4-122">None</span></span>

## <span data-ttu-id="0baf4-123">輸出</span><span class="sxs-lookup"><span data-stu-id="0baf4-123">OUTPUTS</span></span>

### <span data-ttu-id="0baf4-124">System.object. IEnumerable "1 [ASRPolicy，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="0baf4-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0baf4-125">筆記</span><span class="sxs-lookup"><span data-stu-id="0baf4-125">NOTES</span></span>

## <span data-ttu-id="0baf4-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="0baf4-126">RELATED LINKS</span></span>

[<span data-ttu-id="0baf4-127">新-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0baf4-127">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="0baf4-128">移除-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0baf4-128">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
