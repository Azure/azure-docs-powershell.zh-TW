---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 42a0a96a32bf1b7f556ee2787f43a5777afa1115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454055"
---
# <span data-ttu-id="32b1f-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="32b1f-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="32b1f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="32b1f-103">取得受複製受保護專案的可用復原點數。</span><span class="sxs-lookup"><span data-stu-id="32b1f-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32b1f-104">句法</span><span class="sxs-lookup"><span data-stu-id="32b1f-104">SYNTAX</span></span>

### <span data-ttu-id="32b1f-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="32b1f-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32b1f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="32b1f-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32b1f-107">說明</span><span class="sxs-lookup"><span data-stu-id="32b1f-107">DESCRIPTION</span></span>
<span data-ttu-id="32b1f-108">**AzureRmSiteRecoveryRecoveryPoint** Cmdlet 會取得受複製受保護專案的可用復原點數清單。</span><span class="sxs-lookup"><span data-stu-id="32b1f-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="32b1f-109">示例</span><span class="sxs-lookup"><span data-stu-id="32b1f-109">EXAMPLES</span></span>

## <span data-ttu-id="32b1f-110">參數</span><span class="sxs-lookup"><span data-stu-id="32b1f-110">PARAMETERS</span></span>

### <span data-ttu-id="32b1f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b1f-111">-DefaultProfile</span></span>
<span data-ttu-id="32b1f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32b1f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32b1f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="32b1f-113">-Name</span></span>
<span data-ttu-id="32b1f-114">指定此 Cmdlet 取得的復原點名稱。</span><span class="sxs-lookup"><span data-stu-id="32b1f-114">Specifies the name of the recovery point this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b1f-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="32b1f-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="32b1f-116">指定 Azure Site Recovery 複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="32b1f-116">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32b1f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b1f-117">CommonParameters</span></span>
<span data-ttu-id="32b1f-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32b1f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b1f-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32b1f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b1f-120">輸入</span><span class="sxs-lookup"><span data-stu-id="32b1f-120">INPUTS</span></span>

### <span data-ttu-id="32b1f-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="32b1f-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="32b1f-122">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="32b1f-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="32b1f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="32b1f-123">OUTPUTS</span></span>

### <span data-ttu-id="32b1f-124">System.object. IEnumerable "1 [ASRRecoveryPoint，SiteRecovery，Version = 2.0.1.0，Culture = 中性，PublicKeyToken = null]] （SiteRecovery =，Culture = 中立）</span><span class="sxs-lookup"><span data-stu-id="32b1f-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="32b1f-125">筆記</span><span class="sxs-lookup"><span data-stu-id="32b1f-125">NOTES</span></span>

## <span data-ttu-id="32b1f-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="32b1f-126">RELATED LINKS</span></span>

[<span data-ttu-id="32b1f-127">編輯-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="32b1f-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="32b1f-128">AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="32b1f-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="32b1f-129">新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="32b1f-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="32b1f-130">移除-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="32b1f-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="32b1f-131">更新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="32b1f-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
