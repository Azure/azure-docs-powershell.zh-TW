---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8dcab2bcaeafbc5304de72b8bcf539a6f4a53934
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126265"
---
# <span data-ttu-id="472e2-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="472e2-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="472e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="472e2-102">SYNOPSIS</span></span>
<span data-ttu-id="472e2-103">刪除指定的 ASR 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="472e2-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="472e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="472e2-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="472e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="472e2-105">DESCRIPTION</span></span>
<span data-ttu-id="472e2-106">**AzRecoveryServicesAsrStorageClassificationMapping** Cmdlet 會刪除指定的 Azure Site Recovery 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="472e2-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="472e2-107">示例</span><span class="sxs-lookup"><span data-stu-id="472e2-107">EXAMPLES</span></span>

### <span data-ttu-id="472e2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="472e2-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="472e2-109">開始刪除指定的儲存分類對應，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="472e2-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="472e2-110">參數</span><span class="sxs-lookup"><span data-stu-id="472e2-110">PARAMETERS</span></span>

### <span data-ttu-id="472e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="472e2-111">-DefaultProfile</span></span>
<span data-ttu-id="472e2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="472e2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="472e2-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="472e2-113">-InputObject</span></span>
<span data-ttu-id="472e2-114">Cmdlet 的輸入物件：與要刪除之 ASR 儲存分類對應的 ASR 儲存分類對應物件。</span><span class="sxs-lookup"><span data-stu-id="472e2-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="472e2-115">-確認</span><span class="sxs-lookup"><span data-stu-id="472e2-115">-Confirm</span></span>
<span data-ttu-id="472e2-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="472e2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="472e2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="472e2-117">-WhatIf</span></span>
<span data-ttu-id="472e2-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="472e2-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="472e2-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="472e2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="472e2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="472e2-120">CommonParameters</span></span>
<span data-ttu-id="472e2-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="472e2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="472e2-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="472e2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="472e2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="472e2-123">INPUTS</span></span>

### <span data-ttu-id="472e2-124">RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="472e2-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="472e2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="472e2-125">OUTPUTS</span></span>

### <span data-ttu-id="472e2-126">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="472e2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="472e2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="472e2-127">NOTES</span></span>

## <span data-ttu-id="472e2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="472e2-128">RELATED LINKS</span></span>

[<span data-ttu-id="472e2-129">AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="472e2-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="472e2-130">新-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="472e2-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
