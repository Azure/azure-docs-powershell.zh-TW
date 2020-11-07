---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 8bea83b033ffb8a2e56ba6d28759e88280529a2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624692"
---
# <span data-ttu-id="83e0c-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="83e0c-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="83e0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="83e0c-103">取得在復原服務電子倉庫中) ASR 儲存空間分類中發現的可用 (。</span><span class="sxs-lookup"><span data-stu-id="83e0c-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83e0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="83e0c-104">SYNTAX</span></span>

### <span data-ttu-id="83e0c-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="83e0c-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83e0c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="83e0c-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83e0c-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="83e0c-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83e0c-108">說明</span><span class="sxs-lookup"><span data-stu-id="83e0c-108">DESCRIPTION</span></span>
<span data-ttu-id="83e0c-109">**AzureRmRecoveryServicesAsrStorageClassification** Cmdlet 會在復原服務電子倉庫中取得已探索之 ASR 儲存空間分類的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="83e0c-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="83e0c-110">示例</span><span class="sxs-lookup"><span data-stu-id="83e0c-110">EXAMPLES</span></span>

### <span data-ttu-id="83e0c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="83e0c-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="83e0c-112">列出與指定的 ASR 結構相對應的已探索儲存分類。</span><span class="sxs-lookup"><span data-stu-id="83e0c-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="83e0c-113">參數</span><span class="sxs-lookup"><span data-stu-id="83e0c-113">PARAMETERS</span></span>

### <span data-ttu-id="83e0c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e0c-114">-DefaultProfile</span></span>
<span data-ttu-id="83e0c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="83e0c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="83e0c-116">-結構</span><span class="sxs-lookup"><span data-stu-id="83e0c-116">-Fabric</span></span>
<span data-ttu-id="83e0c-117">指定 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="83e0c-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="83e0c-118">這個 Cmdlet 會取得與指定的 ASR 結構相對應的已探索儲存空間分類的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="83e0c-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83e0c-119">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="83e0c-119">-FriendlyName</span></span>
<span data-ttu-id="83e0c-120">指定要取得的儲存分類物件的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="83e0c-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e0c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="83e0c-121">-Name</span></span>
<span data-ttu-id="83e0c-122">指定要取得之儲存分類物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="83e0c-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="83e0c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e0c-123">CommonParameters</span></span>
<span data-ttu-id="83e0c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83e0c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e0c-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83e0c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e0c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="83e0c-126">INPUTS</span></span>

### <span data-ttu-id="83e0c-127">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="83e0c-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="83e0c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="83e0c-128">OUTPUTS</span></span>

### <span data-ttu-id="83e0c-129">System.object. IEnumerable "1 [ASRStorageClassification，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="83e0c-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="83e0c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="83e0c-130">NOTES</span></span>

## <span data-ttu-id="83e0c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="83e0c-131">RELATED LINKS</span></span>
