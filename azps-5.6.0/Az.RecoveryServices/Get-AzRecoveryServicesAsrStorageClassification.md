---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 441e3108053aa55c93ab0f9ee150bebd592a091e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910398"
---
# <span data-ttu-id="4be03-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="4be03-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="4be03-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4be03-102">SYNOPSIS</span></span>
<span data-ttu-id="4be03-103">在修復服務 (中) ASR 儲存分類的可用選項。</span><span class="sxs-lookup"><span data-stu-id="4be03-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="4be03-104">語法</span><span class="sxs-lookup"><span data-stu-id="4be03-104">SYNTAX</span></span>

### <span data-ttu-id="4be03-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="4be03-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4be03-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4be03-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be03-107">ByObjectWithWithWithLyName</span><span class="sxs-lookup"><span data-stu-id="4be03-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4be03-108">描述</span><span class="sxs-lookup"><span data-stu-id="4be03-108">DESCRIPTION</span></span>
<span data-ttu-id="4be03-109">**Get-AzRecoveryServicesAsrStorageClassification** Cmdlet 會取得修復服務保存庫中所發現 ASR 儲存分類的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4be03-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="4be03-110">例子</span><span class="sxs-lookup"><span data-stu-id="4be03-110">EXAMPLES</span></span>

### <span data-ttu-id="4be03-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="4be03-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="4be03-112">列出與指定的 ASR 布料對應的已發現儲存分類。</span><span class="sxs-lookup"><span data-stu-id="4be03-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="4be03-113">參數</span><span class="sxs-lookup"><span data-stu-id="4be03-113">PARAMETERS</span></span>

### <span data-ttu-id="4be03-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be03-114">-DefaultProfile</span></span>
<span data-ttu-id="4be03-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4be03-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4be03-116">-布料</span><span class="sxs-lookup"><span data-stu-id="4be03-116">-Fabric</span></span>
<span data-ttu-id="4be03-117">指定 ASR 布料物件。</span><span class="sxs-lookup"><span data-stu-id="4be03-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="4be03-118">Cmdlet 會獲得與指定 ASR 布料對應的已發現儲存區分類詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4be03-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="4be03-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4be03-119">-FriendlyName</span></span>
<span data-ttu-id="4be03-120">指定要取得之儲存分類物件的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="4be03-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="4be03-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4be03-121">-Name</span></span>
<span data-ttu-id="4be03-122">指定要取得之儲存分類物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="4be03-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="4be03-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be03-123">CommonParameters</span></span>
<span data-ttu-id="4be03-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4be03-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be03-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4be03-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be03-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4be03-126">INPUTS</span></span>

### <span data-ttu-id="4be03-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4be03-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4be03-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4be03-128">OUTPUTS</span></span>

### <span data-ttu-id="4be03-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="4be03-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="4be03-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4be03-130">NOTES</span></span>

## <span data-ttu-id="4be03-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4be03-131">RELATED LINKS</span></span>
