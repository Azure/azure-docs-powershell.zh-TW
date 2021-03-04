---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8ad9ca87687acfdeb526dc33cdcb5a6ec70c65bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902277"
---
# <span data-ttu-id="277a7-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="277a7-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="277a7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="277a7-102">SYNOPSIS</span></span>
<span data-ttu-id="277a7-103">在修復服務保存庫中建立 ASR 儲存分類地圖。</span><span class="sxs-lookup"><span data-stu-id="277a7-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="277a7-104">語法</span><span class="sxs-lookup"><span data-stu-id="277a7-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="277a7-105">描述</span><span class="sxs-lookup"><span data-stu-id="277a7-105">DESCRIPTION</span></span>
<span data-ttu-id="277a7-106">**New-AzRecoveryServicesAsrStorageClassificationMadlet** 會建立一個儲存分類來與修復服務保存庫進行地圖。</span><span class="sxs-lookup"><span data-stu-id="277a7-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="277a7-107">例子</span><span class="sxs-lookup"><span data-stu-id="277a7-107">EXAMPLES</span></span>

### <span data-ttu-id="277a7-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="277a7-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="277a7-109">使用指定的參數啟動儲存分類地圖建立作業，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="277a7-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="277a7-110">參數</span><span class="sxs-lookup"><span data-stu-id="277a7-110">PARAMETERS</span></span>

### <span data-ttu-id="277a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277a7-111">-DefaultProfile</span></span>
<span data-ttu-id="277a7-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="277a7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="277a7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="277a7-113">-Name</span></span>
<span data-ttu-id="277a7-114">指定 ASR 儲存分類地圖的名稱。</span><span class="sxs-lookup"><span data-stu-id="277a7-114">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277a7-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="277a7-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="277a7-116">指定地圖的主要 ASR 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="277a7-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="277a7-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="277a7-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="277a7-118">指定該地圖的復原 ASR 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="277a7-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277a7-119">-確認</span><span class="sxs-lookup"><span data-stu-id="277a7-119">-Confirm</span></span>
<span data-ttu-id="277a7-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="277a7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="277a7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="277a7-121">-WhatIf</span></span>
<span data-ttu-id="277a7-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="277a7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="277a7-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="277a7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="277a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277a7-124">CommonParameters</span></span>
<span data-ttu-id="277a7-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="277a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277a7-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="277a7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277a7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="277a7-127">INPUTS</span></span>

### <span data-ttu-id="277a7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="277a7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="277a7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="277a7-129">OUTPUTS</span></span>

### <span data-ttu-id="277a7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="277a7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="277a7-131">筆記</span><span class="sxs-lookup"><span data-stu-id="277a7-131">NOTES</span></span>

## <span data-ttu-id="277a7-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="277a7-132">RELATED LINKS</span></span>

[<span data-ttu-id="277a7-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="277a7-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="277a7-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="277a7-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
