---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 857bc438d1c51b28e3ead1095ca4722fce7ccc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903433"
---
# <span data-ttu-id="7a5d0-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="7a5d0-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="7a5d0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7a5d0-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5d0-103">為要複製的 vMWare 虛擬機器磁片建立磁片映射物件。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="7a5d0-104">語法</span><span class="sxs-lookup"><span data-stu-id="7a5d0-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a5d0-105">描述</span><span class="sxs-lookup"><span data-stu-id="7a5d0-105">DESCRIPTION</span></span>
<span data-ttu-id="7a5d0-106">建立將 vMWare 虛擬機器磁片與緩存儲存帳戶及目標受管理磁片類型 (修復區域) 以用於複製磁片的磁片地圖物件。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="7a5d0-107">例子</span><span class="sxs-lookup"><span data-stu-id="7a5d0-107">EXAMPLES</span></span>

### <span data-ttu-id="7a5d0-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="7a5d0-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="7a5d0-109">建立要複製之 vMWare 虛擬機器磁片的磁片映射物件。在啟用 vMWare 電腦保護期間使用。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="7a5d0-110">參數</span><span class="sxs-lookup"><span data-stu-id="7a5d0-110">PARAMETERS</span></span>

### <span data-ttu-id="7a5d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5d0-111">-DefaultProfile</span></span>
<span data-ttu-id="7a5d0-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a5d0-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="7a5d0-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="7a5d0-114">指定磁片加密集的資源識別碼，用來加密受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="7a5d0-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="7a5d0-115">-DiskId</span></span>
<span data-ttu-id="7a5d0-116">指定此對應對應的磁片的 DiskId。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="7a5d0-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="7a5d0-117">-DiskType</span></span>
<span data-ttu-id="7a5d0-118">指定修復磁片類型。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="7a5d0-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7a5d0-119">-LogStorageAccountId</span></span>
<span data-ttu-id="7a5d0-120">指定要用來儲存複製記錄之記錄或緩存儲存帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="7a5d0-121">-確認</span><span class="sxs-lookup"><span data-stu-id="7a5d0-121">-Confirm</span></span>
<span data-ttu-id="7a5d0-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a5d0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a5d0-123">-WhatIf</span></span>
<span data-ttu-id="7a5d0-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a5d0-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a5d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5d0-126">CommonParameters</span></span>
<span data-ttu-id="7a5d0-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7a5d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5d0-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a5d0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5d0-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7a5d0-129">INPUTS</span></span>

### <span data-ttu-id="7a5d0-130">沒有</span><span class="sxs-lookup"><span data-stu-id="7a5d0-130">None</span></span>

## <span data-ttu-id="7a5d0-131">輸出</span><span class="sxs-lookup"><span data-stu-id="7a5d0-131">OUTPUTS</span></span>

### <span data-ttu-id="7a5d0-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2CoverInput</span><span class="sxs-lookup"><span data-stu-id="7a5d0-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="7a5d0-133">筆記</span><span class="sxs-lookup"><span data-stu-id="7a5d0-133">NOTES</span></span>

## <span data-ttu-id="7a5d0-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a5d0-134">RELATED LINKS</span></span>
