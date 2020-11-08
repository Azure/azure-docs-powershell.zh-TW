---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126268"
---
# <span data-ttu-id="e8449-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e8449-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="e8449-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8449-102">SYNOPSIS</span></span>
<span data-ttu-id="e8449-103">取得在復原服務電子倉庫中) ASR 儲存空間分類中發現的可用 (。</span><span class="sxs-lookup"><span data-stu-id="e8449-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="e8449-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8449-104">SYNTAX</span></span>

### <span data-ttu-id="e8449-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="e8449-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8449-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e8449-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8449-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e8449-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8449-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8449-108">DESCRIPTION</span></span>
<span data-ttu-id="e8449-109">**AzRecoveryServicesAsrStorageClassification** Cmdlet 會在復原服務電子倉庫中取得已探索之 ASR 儲存空間分類的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e8449-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="e8449-110">示例</span><span class="sxs-lookup"><span data-stu-id="e8449-110">EXAMPLES</span></span>

### <span data-ttu-id="e8449-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e8449-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="e8449-112">列出與指定的 ASR 結構相對應的已探索儲存分類。</span><span class="sxs-lookup"><span data-stu-id="e8449-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="e8449-113">參數</span><span class="sxs-lookup"><span data-stu-id="e8449-113">PARAMETERS</span></span>

### <span data-ttu-id="e8449-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8449-114">-DefaultProfile</span></span>
<span data-ttu-id="e8449-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8449-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e8449-116">-結構</span><span class="sxs-lookup"><span data-stu-id="e8449-116">-Fabric</span></span>
<span data-ttu-id="e8449-117">指定 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="e8449-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="e8449-118">這個 Cmdlet 會取得與指定的 ASR 結構相對應的已探索儲存空間分類的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e8449-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8449-119">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e8449-119">-FriendlyName</span></span>
<span data-ttu-id="e8449-120">指定要取得的儲存分類物件的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="e8449-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8449-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8449-121">-Name</span></span>
<span data-ttu-id="e8449-122">指定要取得之儲存分類物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8449-122">Specifies the name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8449-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8449-123">CommonParameters</span></span>
<span data-ttu-id="e8449-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8449-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8449-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8449-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8449-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e8449-126">INPUTS</span></span>

### <span data-ttu-id="e8449-127">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e8449-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e8449-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e8449-128">OUTPUTS</span></span>

### <span data-ttu-id="e8449-129">RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e8449-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="e8449-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e8449-130">NOTES</span></span>

## <span data-ttu-id="e8449-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8449-131">RELATED LINKS</span></span>
