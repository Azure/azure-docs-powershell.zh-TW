---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439087"
---
# <span data-ttu-id="0a8bc-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="0a8bc-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="0a8bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8bc-103">取得在復原服務電子倉庫中) ASR 儲存空間分類中發現的可用 (。</span><span class="sxs-lookup"><span data-stu-id="0a8bc-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="0a8bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a8bc-104">SYNTAX</span></span>

### <span data-ttu-id="0a8bc-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="0a8bc-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a8bc-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="0a8bc-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a8bc-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0a8bc-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a8bc-108">說明</span><span class="sxs-lookup"><span data-stu-id="0a8bc-108">DESCRIPTION</span></span>
<span data-ttu-id="0a8bc-109">**AzRecoveryServicesAsrStorageClassification** Cmdlet 會在復原服務電子倉庫中取得已探索之 ASR 儲存空間分類的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0a8bc-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="0a8bc-110">示例</span><span class="sxs-lookup"><span data-stu-id="0a8bc-110">EXAMPLES</span></span>

### <span data-ttu-id="0a8bc-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0a8bc-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="0a8bc-112">列出與指定的 ASR 結構相對應的已探索儲存分類。</span><span class="sxs-lookup"><span data-stu-id="0a8bc-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="0a8bc-113">參數</span><span class="sxs-lookup"><span data-stu-id="0a8bc-113">PARAMETERS</span></span>

### <span data-ttu-id="0a8bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8bc-114">-DefaultProfile</span></span>
<span data-ttu-id="0a8bc-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a8bc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0a8bc-116">-結構</span><span class="sxs-lookup"><span data-stu-id="0a8bc-116">-Fabric</span></span>
<span data-ttu-id="0a8bc-117">指定 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="0a8bc-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="0a8bc-118">這個 Cmdlet 會取得與指定的 ASR 結構相對應的已探索儲存空間分類的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0a8bc-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="0a8bc-119">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0a8bc-119">-FriendlyName</span></span>
<span data-ttu-id="0a8bc-120">指定要取得的儲存分類物件的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="0a8bc-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="0a8bc-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a8bc-121">-Name</span></span>
<span data-ttu-id="0a8bc-122">指定要取得之儲存分類物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a8bc-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="0a8bc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8bc-123">CommonParameters</span></span>
<span data-ttu-id="0a8bc-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a8bc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8bc-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0a8bc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8bc-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0a8bc-126">INPUTS</span></span>

### <span data-ttu-id="0a8bc-127">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="0a8bc-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="0a8bc-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0a8bc-128">OUTPUTS</span></span>

### <span data-ttu-id="0a8bc-129">RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="0a8bc-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="0a8bc-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0a8bc-130">NOTES</span></span>

## <span data-ttu-id="0a8bc-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a8bc-131">RELATED LINKS</span></span>
