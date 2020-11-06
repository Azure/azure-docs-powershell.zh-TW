---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446695"
---
# <span data-ttu-id="936fa-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="936fa-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="936fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="936fa-102">SYNOPSIS</span></span>
<span data-ttu-id="936fa-103">取得 Azure 網站恢復結構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="936fa-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="936fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="936fa-104">SYNTAX</span></span>

### <span data-ttu-id="936fa-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="936fa-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### <span data-ttu-id="936fa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="936fa-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="936fa-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="936fa-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="936fa-108">說明</span><span class="sxs-lookup"><span data-stu-id="936fa-108">DESCRIPTION</span></span>
<span data-ttu-id="936fa-109">**AzureRmRecoveryServicesAsrFabric** Cmdlet 會取得指定 Azure 網站復原結構的屬性，或在恢復服務電子倉庫中的所有 azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="936fa-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="936fa-110">示例</span><span class="sxs-lookup"><span data-stu-id="936fa-110">EXAMPLES</span></span>

### <span data-ttu-id="936fa-111">範例1</span><span class="sxs-lookup"><span data-stu-id="936fa-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="936fa-112">傳回保存庫中的所有 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="936fa-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

## <span data-ttu-id="936fa-113">參數</span><span class="sxs-lookup"><span data-stu-id="936fa-113">PARAMETERS</span></span>

### <span data-ttu-id="936fa-114">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="936fa-114">-FriendlyName</span></span>
<span data-ttu-id="936fa-115">依結構的易記名稱搜尋 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="936fa-115">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="936fa-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="936fa-116">-Name</span></span>
<span data-ttu-id="936fa-117">透過結構的名稱搜尋 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="936fa-117">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="936fa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="936fa-118">CommonParameters</span></span>
<span data-ttu-id="936fa-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="936fa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="936fa-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="936fa-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="936fa-121">輸入</span><span class="sxs-lookup"><span data-stu-id="936fa-121">INPUTS</span></span>

### <span data-ttu-id="936fa-122">所有</span><span class="sxs-lookup"><span data-stu-id="936fa-122">None</span></span>

## <span data-ttu-id="936fa-123">輸出</span><span class="sxs-lookup"><span data-stu-id="936fa-123">OUTPUTS</span></span>

### <span data-ttu-id="936fa-124">[System.object]. 清單 ' 1 [RecoveryServices. SiteRecovery，ASRFabric，，RecoveryServices. SiteRecovery，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="936fa-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="936fa-125">筆記</span><span class="sxs-lookup"><span data-stu-id="936fa-125">NOTES</span></span>

## <span data-ttu-id="936fa-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="936fa-126">RELATED LINKS</span></span>

[<span data-ttu-id="936fa-127">新-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="936fa-127">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="936fa-128">移除-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="936fa-128">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
