---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966144"
---
# <span data-ttu-id="12b8d-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="12b8d-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="12b8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="12b8d-103">建立要複製之 vMWare 虛擬機器磁片的磁片對應物件。</span><span class="sxs-lookup"><span data-stu-id="12b8d-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="12b8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="12b8d-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12b8d-105">說明</span><span class="sxs-lookup"><span data-stu-id="12b8d-105">DESCRIPTION</span></span>
<span data-ttu-id="12b8d-106">建立磁片對應物件，該物件會將 vMWare 虛擬機器磁片對應至快取儲存空間帳戶，並將目標受管理的磁片類型 (復原區域) ，以用於複製磁片。</span><span class="sxs-lookup"><span data-stu-id="12b8d-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="12b8d-107">示例</span><span class="sxs-lookup"><span data-stu-id="12b8d-107">EXAMPLES</span></span>

### <span data-ttu-id="12b8d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="12b8d-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="12b8d-109">建立要複製之 vMWare 虛擬機器磁片的磁片對應物件。在 vMWare 電腦的 [啟用保護] 期間使用。</span><span class="sxs-lookup"><span data-stu-id="12b8d-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="12b8d-110">參數</span><span class="sxs-lookup"><span data-stu-id="12b8d-110">PARAMETERS</span></span>

### <span data-ttu-id="12b8d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b8d-111">-DefaultProfile</span></span>
<span data-ttu-id="12b8d-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12b8d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12b8d-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="12b8d-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="12b8d-114">指定磁片加密集的資源識別碼，以用於加密受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="12b8d-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b8d-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="12b8d-115">-DiskId</span></span>
<span data-ttu-id="12b8d-116">指定此對應對應之磁片的 DiskId。</span><span class="sxs-lookup"><span data-stu-id="12b8d-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="12b8d-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="12b8d-117">-DiskType</span></span>
<span data-ttu-id="12b8d-118">指定恢復磁片類型。</span><span class="sxs-lookup"><span data-stu-id="12b8d-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="12b8d-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="12b8d-119">-LogStorageAccountId</span></span>
<span data-ttu-id="12b8d-120">指定要用來儲存複製記錄的記錄或快取儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="12b8d-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="12b8d-121">-確認</span><span class="sxs-lookup"><span data-stu-id="12b8d-121">-Confirm</span></span>
<span data-ttu-id="12b8d-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12b8d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12b8d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12b8d-123">-WhatIf</span></span>
<span data-ttu-id="12b8d-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12b8d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12b8d-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12b8d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12b8d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b8d-126">CommonParameters</span></span>
<span data-ttu-id="12b8d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12b8d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b8d-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="12b8d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b8d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="12b8d-129">INPUTS</span></span>

### <span data-ttu-id="12b8d-130">所有</span><span class="sxs-lookup"><span data-stu-id="12b8d-130">None</span></span>

## <span data-ttu-id="12b8d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="12b8d-131">OUTPUTS</span></span>

### <span data-ttu-id="12b8d-132">RecoveryServices. SiteRecovery. AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="12b8d-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="12b8d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="12b8d-133">NOTES</span></span>

## <span data-ttu-id="12b8d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="12b8d-134">RELATED LINKS</span></span>
