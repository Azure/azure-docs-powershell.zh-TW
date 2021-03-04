---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c5dea86066fd2b7bc6bd3b2bd3eb7ac94f401895
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904874"
---
# <span data-ttu-id="69be6-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="69be6-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="69be6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="69be6-102">SYNOPSIS</span></span>
<span data-ttu-id="69be6-103">獲得 ASR 儲存分類地圖。</span><span class="sxs-lookup"><span data-stu-id="69be6-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="69be6-104">語法</span><span class="sxs-lookup"><span data-stu-id="69be6-104">SYNTAX</span></span>

### <span data-ttu-id="69be6-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="69be6-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69be6-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="69be6-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69be6-107">描述</span><span class="sxs-lookup"><span data-stu-id="69be6-107">DESCRIPTION</span></span>
<span data-ttu-id="69be6-108">**Get-AzRecoveryServicesAsrStorageClassificationMadlet** Cmdlet 會取得 ASR 儲存分類地圖的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="69be6-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="69be6-109">例子</span><span class="sxs-lookup"><span data-stu-id="69be6-109">EXAMPLES</span></span>

### <span data-ttu-id="69be6-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="69be6-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="69be6-111">列出對應到指定儲存分類的所有儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="69be6-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="69be6-112">參數</span><span class="sxs-lookup"><span data-stu-id="69be6-112">PARAMETERS</span></span>

### <span data-ttu-id="69be6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69be6-113">-DefaultProfile</span></span>
<span data-ttu-id="69be6-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="69be6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="69be6-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="69be6-115">-Name</span></span>
<span data-ttu-id="69be6-116">指定要取得的儲存分類地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="69be6-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="69be6-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="69be6-117">-StorageClassification</span></span>
<span data-ttu-id="69be6-118">指定 ASR 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="69be6-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="69be6-119">Cmdlet 會獲得對應到指定儲存分類的 ASR 儲存分類對應</span><span class="sxs-lookup"><span data-stu-id="69be6-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69be6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69be6-120">CommonParameters</span></span>
<span data-ttu-id="69be6-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="69be6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69be6-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69be6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69be6-123">輸入</span><span class="sxs-lookup"><span data-stu-id="69be6-123">INPUTS</span></span>

### <span data-ttu-id="69be6-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="69be6-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="69be6-125">輸出</span><span class="sxs-lookup"><span data-stu-id="69be6-125">OUTPUTS</span></span>

### <span data-ttu-id="69be6-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="69be6-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="69be6-127">筆記</span><span class="sxs-lookup"><span data-stu-id="69be6-127">NOTES</span></span>

## <span data-ttu-id="69be6-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="69be6-128">RELATED LINKS</span></span>

[<span data-ttu-id="69be6-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="69be6-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="69be6-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="69be6-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
