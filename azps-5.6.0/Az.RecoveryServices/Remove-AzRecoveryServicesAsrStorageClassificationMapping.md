---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: b19808ff7b5576c93bc81414d665e23086e524d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902206"
---
# <span data-ttu-id="7c73f-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7c73f-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="7c73f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7c73f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c73f-103">刪除指定的 ASR 儲存分類地圖。</span><span class="sxs-lookup"><span data-stu-id="7c73f-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="7c73f-104">語法</span><span class="sxs-lookup"><span data-stu-id="7c73f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c73f-105">描述</span><span class="sxs-lookup"><span data-stu-id="7c73f-105">DESCRIPTION</span></span>
<span data-ttu-id="7c73f-106">**Remove-AzRecoveryServicesAsrStorageClassificationMadlet** Cmdlet 會刪除指定的 Azure 網站復原儲存分類地圖。</span><span class="sxs-lookup"><span data-stu-id="7c73f-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="7c73f-107">例子</span><span class="sxs-lookup"><span data-stu-id="7c73f-107">EXAMPLES</span></span>

### <span data-ttu-id="7c73f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="7c73f-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="7c73f-109">開始刪除指定的儲存分類地圖，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="7c73f-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7c73f-110">參數</span><span class="sxs-lookup"><span data-stu-id="7c73f-110">PARAMETERS</span></span>

### <span data-ttu-id="7c73f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c73f-111">-DefaultProfile</span></span>
<span data-ttu-id="7c73f-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c73f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7c73f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c73f-113">-InputObject</span></span>
<span data-ttu-id="7c73f-114">Cmdlet 的輸入物件：對應至要刪除之 ASR 儲存分類對應物件的 ASR 儲存分類對應物件。</span><span class="sxs-lookup"><span data-stu-id="7c73f-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c73f-115">-確認</span><span class="sxs-lookup"><span data-stu-id="7c73f-115">-Confirm</span></span>
<span data-ttu-id="7c73f-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7c73f-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c73f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c73f-117">-WhatIf</span></span>
<span data-ttu-id="7c73f-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c73f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c73f-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c73f-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c73f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c73f-120">CommonParameters</span></span>
<span data-ttu-id="7c73f-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7c73f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c73f-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c73f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c73f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7c73f-123">INPUTS</span></span>

### <span data-ttu-id="7c73f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7c73f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="7c73f-125">輸出</span><span class="sxs-lookup"><span data-stu-id="7c73f-125">OUTPUTS</span></span>

### <span data-ttu-id="7c73f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="7c73f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7c73f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="7c73f-127">NOTES</span></span>

## <span data-ttu-id="7c73f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c73f-128">RELATED LINKS</span></span>

[<span data-ttu-id="7c73f-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7c73f-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="7c73f-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7c73f-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
