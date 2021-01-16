---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282959"
---
# <span data-ttu-id="5cc96-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5cc96-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="5cc96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5cc96-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc96-103">在 [恢復服務] 保存庫中建立 ASR 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="5cc96-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="5cc96-104">句法</span><span class="sxs-lookup"><span data-stu-id="5cc96-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cc96-105">說明</span><span class="sxs-lookup"><span data-stu-id="5cc96-105">DESCRIPTION</span></span>
<span data-ttu-id="5cc96-106">**AzRecoveryServicesAsrStorageClassificationMapping** Cmdlet 會建立 [恢復服務] 保存庫的儲存分類。</span><span class="sxs-lookup"><span data-stu-id="5cc96-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="5cc96-107">示例</span><span class="sxs-lookup"><span data-stu-id="5cc96-107">EXAMPLES</span></span>

### <span data-ttu-id="5cc96-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5cc96-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="5cc96-109">使用指定的參數啟動儲存分類對應建立作業，並傳回用來追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="5cc96-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5cc96-110">參數</span><span class="sxs-lookup"><span data-stu-id="5cc96-110">PARAMETERS</span></span>

### <span data-ttu-id="5cc96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc96-111">-DefaultProfile</span></span>
<span data-ttu-id="5cc96-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5cc96-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5cc96-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="5cc96-113">-Name</span></span>
<span data-ttu-id="5cc96-114">指定 ASR 儲存分類對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="5cc96-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="5cc96-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="5cc96-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="5cc96-116">指定對應的主要 ASR 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="5cc96-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="5cc96-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="5cc96-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="5cc96-118">指定對應的 [恢復 ASR] 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="5cc96-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="5cc96-119">-確認</span><span class="sxs-lookup"><span data-stu-id="5cc96-119">-Confirm</span></span>
<span data-ttu-id="5cc96-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5cc96-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc96-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc96-121">-WhatIf</span></span>
<span data-ttu-id="5cc96-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5cc96-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cc96-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5cc96-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cc96-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc96-124">CommonParameters</span></span>
<span data-ttu-id="5cc96-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5cc96-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc96-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5cc96-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc96-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5cc96-127">INPUTS</span></span>

### <span data-ttu-id="5cc96-128">RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="5cc96-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="5cc96-129">輸出</span><span class="sxs-lookup"><span data-stu-id="5cc96-129">OUTPUTS</span></span>

### <span data-ttu-id="5cc96-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5cc96-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5cc96-131">筆記</span><span class="sxs-lookup"><span data-stu-id="5cc96-131">NOTES</span></span>

## <span data-ttu-id="5cc96-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="5cc96-132">RELATED LINKS</span></span>

[<span data-ttu-id="5cc96-133">AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5cc96-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="5cc96-134">移除-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5cc96-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
