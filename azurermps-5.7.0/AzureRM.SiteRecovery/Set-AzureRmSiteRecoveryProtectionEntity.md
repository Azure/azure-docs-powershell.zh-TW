---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 21bf19ba4a4d17ef41f6741deedd5cac486bbb32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623956"
---
# <span data-ttu-id="a3b3d-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a3b3d-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="a3b3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b3d-103">設定網站恢復保護實體的狀態。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3b3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3b3d-104">SYNTAX</span></span>

### <span data-ttu-id="a3b3d-105">DisableDR (預設) </span><span class="sxs-lookup"><span data-stu-id="a3b3d-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3b3d-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a3b3d-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3b3d-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="a3b3d-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3b3d-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="a3b3d-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3b3d-109">說明</span><span class="sxs-lookup"><span data-stu-id="a3b3d-109">DESCRIPTION</span></span>
<span data-ttu-id="a3b3d-110">**AzureRmSiteRecoveryProtectionEntity** Cmdlet 可啟用或停用 Azure Site Recovery 保護實體的保護。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="a3b3d-111">示例</span><span class="sxs-lookup"><span data-stu-id="a3b3d-111">EXAMPLES</span></span>

## <span data-ttu-id="a3b3d-112">參數</span><span class="sxs-lookup"><span data-stu-id="a3b3d-112">PARAMETERS</span></span>

### <span data-ttu-id="a3b3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b3d-113">-DefaultProfile</span></span>
<span data-ttu-id="a3b3d-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3b3d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a3b3d-115">-Force</span></span>
<span data-ttu-id="a3b3d-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-117">-OS</span><span class="sxs-lookup"><span data-stu-id="a3b3d-117">-OS</span></span>
<span data-ttu-id="a3b3d-118">指定作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-118">Specifies the operating system type.</span></span>
<span data-ttu-id="a3b3d-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a3b3d-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a3b3d-120">時間</span><span class="sxs-lookup"><span data-stu-id="a3b3d-120">Windows</span></span>
- <span data-ttu-id="a3b3d-121">Linux</span><span class="sxs-lookup"><span data-stu-id="a3b3d-121">Linux</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-122">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="a3b3d-122">-OSDiskName</span></span>
<span data-ttu-id="a3b3d-123">指定包含作業系統的磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-123">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-124">-原則</span><span class="sxs-lookup"><span data-stu-id="a3b3d-124">-Policy</span></span>
<span data-ttu-id="a3b3d-125">指定網站恢復原則物件。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-125">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-126">-保護</span><span class="sxs-lookup"><span data-stu-id="a3b3d-126">-Protection</span></span>
<span data-ttu-id="a3b3d-127">指定是否應啟用或停用保護。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-127">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="a3b3d-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a3b3d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a3b3d-129">啟用</span><span class="sxs-lookup"><span data-stu-id="a3b3d-129">Enable</span></span>
- <span data-ttu-id="a3b3d-130">禁止</span><span class="sxs-lookup"><span data-stu-id="a3b3d-130">Disable</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-131">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a3b3d-131">-ProtectionEntity</span></span>
<span data-ttu-id="a3b3d-132">指定保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-132">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-133">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a3b3d-133">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="a3b3d-134">指定目標 Azure 儲存空間帳戶的 ID。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-134">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-135">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a3b3d-135">-WaitForCompletion</span></span>
<span data-ttu-id="a3b3d-136">表示命令在傳回之前等待完成。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-136">Indicates that the command waits for completion before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-137">-確認</span><span class="sxs-lookup"><span data-stu-id="a3b3d-137">-Confirm</span></span>
<span data-ttu-id="a3b3d-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3b3d-139">-WhatIf</span></span>
<span data-ttu-id="a3b3d-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-140">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a3b3d-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b3d-142">CommonParameters</span></span>
<span data-ttu-id="a3b3d-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b3d-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b3d-145">輸入</span><span class="sxs-lookup"><span data-stu-id="a3b3d-145">INPUTS</span></span>

### <span data-ttu-id="a3b3d-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a3b3d-146">ASRProtectionEntity</span></span>
<span data-ttu-id="a3b3d-147">形參 "ProtectionEntity" 接受管線中 "ASRProtectionEntity" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a3b3d-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="a3b3d-148">輸出</span><span class="sxs-lookup"><span data-stu-id="a3b3d-148">OUTPUTS</span></span>

### <span data-ttu-id="a3b3d-149">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a3b3d-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a3b3d-150">筆記</span><span class="sxs-lookup"><span data-stu-id="a3b3d-150">NOTES</span></span>

## <span data-ttu-id="a3b3d-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3b3d-151">RELATED LINKS</span></span>

[<span data-ttu-id="a3b3d-152">AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a3b3d-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
