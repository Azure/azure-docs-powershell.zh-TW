---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 245eb56ea973c1330b7f8b9d32a3f0b9584bd0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624755"
---
# <span data-ttu-id="6025b-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6025b-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="6025b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6025b-102">SYNOPSIS</span></span>
<span data-ttu-id="6025b-103">設定網站恢復保護實體的狀態。</span><span class="sxs-lookup"><span data-stu-id="6025b-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6025b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6025b-104">SYNTAX</span></span>

### <span data-ttu-id="6025b-105">DisableDR (預設) </span><span class="sxs-lookup"><span data-stu-id="6025b-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6025b-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="6025b-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6025b-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6025b-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6025b-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="6025b-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6025b-109">說明</span><span class="sxs-lookup"><span data-stu-id="6025b-109">DESCRIPTION</span></span>
<span data-ttu-id="6025b-110">**AzureRmSiteRecoveryProtectionEntity** Cmdlet 可啟用或停用 Azure Site Recovery 保護實體的保護。</span><span class="sxs-lookup"><span data-stu-id="6025b-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="6025b-111">示例</span><span class="sxs-lookup"><span data-stu-id="6025b-111">EXAMPLES</span></span>

## <span data-ttu-id="6025b-112">參數</span><span class="sxs-lookup"><span data-stu-id="6025b-112">PARAMETERS</span></span>

### <span data-ttu-id="6025b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6025b-113">-Force</span></span>
<span data-ttu-id="6025b-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6025b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6025b-115">-OS</span><span class="sxs-lookup"><span data-stu-id="6025b-115">-OS</span></span>
<span data-ttu-id="6025b-116">指定作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="6025b-116">Specifies the operating system type.</span></span>
<span data-ttu-id="6025b-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6025b-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6025b-118">時間</span><span class="sxs-lookup"><span data-stu-id="6025b-118">Windows</span></span>
- <span data-ttu-id="6025b-119">Linux</span><span class="sxs-lookup"><span data-stu-id="6025b-119">Linux</span></span>

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

### <span data-ttu-id="6025b-120">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="6025b-120">-OSDiskName</span></span>
<span data-ttu-id="6025b-121">指定包含作業系統的磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="6025b-121">Specifies the name of the disk that contains the operating system.</span></span>

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

### <span data-ttu-id="6025b-122">-原則</span><span class="sxs-lookup"><span data-stu-id="6025b-122">-Policy</span></span>
<span data-ttu-id="6025b-123">指定網站恢復原則物件。</span><span class="sxs-lookup"><span data-stu-id="6025b-123">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6025b-124">-保護</span><span class="sxs-lookup"><span data-stu-id="6025b-124">-Protection</span></span>
<span data-ttu-id="6025b-125">指定是否應啟用或停用保護。</span><span class="sxs-lookup"><span data-stu-id="6025b-125">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="6025b-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6025b-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6025b-127">啟用</span><span class="sxs-lookup"><span data-stu-id="6025b-127">Enable</span></span>
- <span data-ttu-id="6025b-128">禁止</span><span class="sxs-lookup"><span data-stu-id="6025b-128">Disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6025b-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6025b-129">-ProtectionEntity</span></span>
<span data-ttu-id="6025b-130">指定保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="6025b-130">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6025b-131">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6025b-131">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="6025b-132">指定目標 Azure 儲存空間帳戶的 ID。</span><span class="sxs-lookup"><span data-stu-id="6025b-132">Specifies the ID of the target Azure Storage account.</span></span>

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

### <span data-ttu-id="6025b-133">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="6025b-133">-WaitForCompletion</span></span>
<span data-ttu-id="6025b-134">表示命令在傳回之前等待完成。</span><span class="sxs-lookup"><span data-stu-id="6025b-134">Indicates that the command waits for completion before returning.</span></span>

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

### <span data-ttu-id="6025b-135">-確認</span><span class="sxs-lookup"><span data-stu-id="6025b-135">-Confirm</span></span>
<span data-ttu-id="6025b-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6025b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6025b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6025b-137">-WhatIf</span></span>
<span data-ttu-id="6025b-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6025b-138">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6025b-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6025b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6025b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6025b-140">-DefaultProfile</span></span>
<span data-ttu-id="6025b-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6025b-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6025b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6025b-142">CommonParameters</span></span>
<span data-ttu-id="6025b-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6025b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6025b-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6025b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6025b-145">輸入</span><span class="sxs-lookup"><span data-stu-id="6025b-145">INPUTS</span></span>

### <span data-ttu-id="6025b-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6025b-146">ASRProtectionEntity</span></span>
<span data-ttu-id="6025b-147">形參 "ProtectionEntity" 接受管線中 "ASRProtectionEntity" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6025b-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="6025b-148">輸出</span><span class="sxs-lookup"><span data-stu-id="6025b-148">OUTPUTS</span></span>

### <span data-ttu-id="6025b-149">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6025b-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6025b-150">筆記</span><span class="sxs-lookup"><span data-stu-id="6025b-150">NOTES</span></span>

## <span data-ttu-id="6025b-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="6025b-151">RELATED LINKS</span></span>

[<span data-ttu-id="6025b-152">AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6025b-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
