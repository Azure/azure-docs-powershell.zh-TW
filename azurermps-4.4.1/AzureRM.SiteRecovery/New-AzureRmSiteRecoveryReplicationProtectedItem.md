---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: dcd7b85810c78fa772098f24c428b5f9c8c44183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446657"
---
# <span data-ttu-id="c6869-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c6869-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="c6869-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6869-102">SYNOPSIS</span></span>
<span data-ttu-id="c6869-103">透過建立受保護的專案，為可保護的專案啟用複製</span><span class="sxs-lookup"><span data-stu-id="c6869-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6869-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6869-104">SYNTAX</span></span>

### <span data-ttu-id="c6869-105">DisableDR (預設) </span><span class="sxs-lookup"><span data-stu-id="c6869-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6869-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c6869-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6869-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c6869-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6869-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="c6869-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6869-109">說明</span><span class="sxs-lookup"><span data-stu-id="c6869-109">DESCRIPTION</span></span>
<span data-ttu-id="c6869-110">**新的-AzureRmSiteRecoveryReplicationProtectedItem** Cmdlet 會建立新的受保護的複製專案。</span><span class="sxs-lookup"><span data-stu-id="c6869-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="c6869-111">使用此 Cmdlet 來為可保護的專案啟用複製。</span><span class="sxs-lookup"><span data-stu-id="c6869-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="c6869-112">示例</span><span class="sxs-lookup"><span data-stu-id="c6869-112">EXAMPLES</span></span>

## <span data-ttu-id="c6869-113">參數</span><span class="sxs-lookup"><span data-stu-id="c6869-113">PARAMETERS</span></span>

### <span data-ttu-id="c6869-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6869-114">-Name</span></span>
<span data-ttu-id="c6869-115">指定 Azure Site Recovery 複製受保護的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="c6869-115">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6869-116">-OS</span><span class="sxs-lookup"><span data-stu-id="c6869-116">-OS</span></span>
<span data-ttu-id="c6869-117">指定作業系統系列。</span><span class="sxs-lookup"><span data-stu-id="c6869-117">Specifies the operating system family.</span></span>
<span data-ttu-id="c6869-118">此參數可接受的值為： Windows 或 Linux。</span><span class="sxs-lookup"><span data-stu-id="c6869-118">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6869-119">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="c6869-119">-OSDiskName</span></span>
<span data-ttu-id="c6869-120">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6869-120">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6869-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c6869-121">-ProtectableItem</span></span>
<span data-ttu-id="c6869-122">指定 Azure 網站復原的 [復原] 專案。</span><span class="sxs-lookup"><span data-stu-id="c6869-122">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6869-123">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c6869-123">-ProtectionContainerMapping</span></span>
<span data-ttu-id="c6869-124">指定要用於複製的 Azure Site Recovery 保護容器對應物件。</span><span class="sxs-lookup"><span data-stu-id="c6869-124">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6869-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c6869-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="c6869-126">指定此 Cmdlet 複製的 Azure 儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6869-126">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6869-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="c6869-127">-WaitForCompletion</span></span>
<span data-ttu-id="c6869-128">表示 Cmdlet 會等到完成。</span><span class="sxs-lookup"><span data-stu-id="c6869-128">Indicates that the cmdlet waits for completion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6869-129">-確認</span><span class="sxs-lookup"><span data-stu-id="c6869-129">-Confirm</span></span>
<span data-ttu-id="c6869-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6869-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6869-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6869-131">-WhatIf</span></span>
<span data-ttu-id="c6869-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6869-132">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c6869-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6869-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6869-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6869-134">-DefaultProfile</span></span>
<span data-ttu-id="c6869-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6869-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6869-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6869-136">CommonParameters</span></span>
<span data-ttu-id="c6869-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6869-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6869-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6869-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6869-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c6869-139">INPUTS</span></span>

### <span data-ttu-id="c6869-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c6869-140">ASRProtectableItem</span></span>
<span data-ttu-id="c6869-141">形參 "ProtectableItem" 接受管線中 "ASRProtectableItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c6869-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="c6869-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c6869-142">OUTPUTS</span></span>

### <span data-ttu-id="c6869-143">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c6869-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c6869-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c6869-144">NOTES</span></span>

## <span data-ttu-id="c6869-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6869-145">RELATED LINKS</span></span>

[<span data-ttu-id="c6869-146">AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c6869-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="c6869-147">移除-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c6869-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="c6869-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c6869-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
