---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 542e75ed0e6531f5778f9793b678b42f953c15d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444452"
---
# <span data-ttu-id="9392a-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="9392a-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="9392a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9392a-102">SYNOPSIS</span></span>
<span data-ttu-id="9392a-103">建立要複製之 Azure 虛擬機器磁片的磁片對應物件。</span><span class="sxs-lookup"><span data-stu-id="9392a-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9392a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9392a-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9392a-105">說明</span><span class="sxs-lookup"><span data-stu-id="9392a-105">DESCRIPTION</span></span>
<span data-ttu-id="9392a-106">建立磁片對應物件，該物件會將 Azure 虛擬機器磁片對應至快取儲存空間帳戶，並將目標儲存空間帳戶 (復原區域) ，以用於複製磁片。</span><span class="sxs-lookup"><span data-stu-id="9392a-106">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="9392a-107">示例</span><span class="sxs-lookup"><span data-stu-id="9392a-107">EXAMPLES</span></span>

### <span data-ttu-id="9392a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9392a-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="9392a-109">建立要複製之 Azure 虛擬機器磁片的磁片對應物件。在 Azure to Azure EnableDr 和重新保護作業期間使用。</span><span class="sxs-lookup"><span data-stu-id="9392a-109">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="9392a-110">參數</span><span class="sxs-lookup"><span data-stu-id="9392a-110">PARAMETERS</span></span>

### <span data-ttu-id="9392a-111">-確認</span><span class="sxs-lookup"><span data-stu-id="9392a-111">-Confirm</span></span>
<span data-ttu-id="9392a-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9392a-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9392a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9392a-113">-DefaultProfile</span></span>
<span data-ttu-id="9392a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9392a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9392a-115">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9392a-115">-LogStorageAccountId</span></span>
<span data-ttu-id="9392a-116">指定要用來儲存複製記錄的記錄或快取儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="9392a-116">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9392a-117">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9392a-117">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="9392a-118">指定要複製的 Azure 儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="9392a-118">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9392a-119">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="9392a-119">-VhdUri</span></span>
<span data-ttu-id="9392a-120">指定此對應對應之磁片的 VHD URI。</span><span class="sxs-lookup"><span data-stu-id="9392a-120">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9392a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9392a-121">-WhatIf</span></span>
<span data-ttu-id="9392a-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9392a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9392a-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9392a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9392a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9392a-124">CommonParameters</span></span>
<span data-ttu-id="9392a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9392a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9392a-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9392a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9392a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9392a-127">INPUTS</span></span>

### <span data-ttu-id="9392a-128">所有</span><span class="sxs-lookup"><span data-stu-id="9392a-128">None</span></span>

## <span data-ttu-id="9392a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9392a-129">OUTPUTS</span></span>

### <span data-ttu-id="9392a-130">RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="9392a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="9392a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9392a-131">NOTES</span></span>

## <span data-ttu-id="9392a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="9392a-132">RELATED LINKS</span></span>
