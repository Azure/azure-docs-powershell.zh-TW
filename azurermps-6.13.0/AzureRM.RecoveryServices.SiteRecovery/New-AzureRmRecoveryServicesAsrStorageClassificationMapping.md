---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 6ab8102de0deb27c18c6e50f8d78db2f23a5155a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623905"
---
# <span data-ttu-id="d4fae-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d4fae-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="d4fae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4fae-102">SYNOPSIS</span></span>
<span data-ttu-id="d4fae-103">在 [恢復服務] 保存庫中建立 ASR 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="d4fae-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4fae-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4fae-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4fae-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4fae-105">DESCRIPTION</span></span>
<span data-ttu-id="d4fae-106">**AzureRmRecoveryServicesAsrStorageClassificationMapping** Cmdlet 會建立 [恢復服務] 保存庫的儲存分類。</span><span class="sxs-lookup"><span data-stu-id="d4fae-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="d4fae-107">示例</span><span class="sxs-lookup"><span data-stu-id="d4fae-107">EXAMPLES</span></span>

### <span data-ttu-id="d4fae-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d4fae-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="d4fae-109">使用指定的參數啟動儲存分類對應建立作業，並傳回用來追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="d4fae-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d4fae-110">參數</span><span class="sxs-lookup"><span data-stu-id="d4fae-110">PARAMETERS</span></span>

### <span data-ttu-id="d4fae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4fae-111">-DefaultProfile</span></span>
<span data-ttu-id="d4fae-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4fae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4fae-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4fae-113">-Name</span></span>
<span data-ttu-id="d4fae-114">指定 ASR 儲存分類對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4fae-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="d4fae-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d4fae-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="d4fae-116">指定對應的主要 ASR 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="d4fae-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="d4fae-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d4fae-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="d4fae-118">指定對應的 [恢復 ASR] 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="d4fae-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="d4fae-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d4fae-119">-Confirm</span></span>
<span data-ttu-id="d4fae-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4fae-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4fae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4fae-121">-WhatIf</span></span>
<span data-ttu-id="d4fae-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4fae-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4fae-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4fae-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4fae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4fae-124">CommonParameters</span></span>
<span data-ttu-id="d4fae-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4fae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4fae-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4fae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4fae-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d4fae-127">INPUTS</span></span>

### <span data-ttu-id="d4fae-128">RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d4fae-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="d4fae-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d4fae-129">OUTPUTS</span></span>

### <span data-ttu-id="d4fae-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d4fae-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d4fae-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d4fae-131">NOTES</span></span>

## <span data-ttu-id="d4fae-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4fae-132">RELATED LINKS</span></span>

[<span data-ttu-id="d4fae-133">AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d4fae-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="d4fae-134">移除-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d4fae-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
