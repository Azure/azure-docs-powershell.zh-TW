---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8aba5d85e11a6494c4362de4d729c5e7b64106fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454024"
---
# <span data-ttu-id="626dd-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="626dd-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="626dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="626dd-102">SYNOPSIS</span></span>
<span data-ttu-id="626dd-103">在網站還原中建立網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="626dd-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="626dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="626dd-104">SYNTAX</span></span>

### <span data-ttu-id="626dd-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="626dd-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="626dd-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="626dd-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="626dd-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="626dd-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="626dd-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="626dd-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="626dd-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="626dd-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="626dd-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="626dd-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="626dd-111">說明</span><span class="sxs-lookup"><span data-stu-id="626dd-111">DESCRIPTION</span></span>
<span data-ttu-id="626dd-112">**新的-AzureRmSiteRecoveryRecoveryPlan** Cmdlet 會在 Azure Site recovery 中建立恢復方案。</span><span class="sxs-lookup"><span data-stu-id="626dd-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="626dd-113">針對容錯移轉與復原的目的，復原方案會收集群組中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="626dd-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="626dd-114">示例</span><span class="sxs-lookup"><span data-stu-id="626dd-114">EXAMPLES</span></span>

### <span data-ttu-id="626dd-115">範例1：將復原方案新增至網站復原電子倉庫</span><span class="sxs-lookup"><span data-stu-id="626dd-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="626dd-116">這個命令會將名為 RecoveryPlan.xml 的復原方案新增至 Azure Site Recovery 保存庫。</span><span class="sxs-lookup"><span data-stu-id="626dd-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="626dd-117">參數</span><span class="sxs-lookup"><span data-stu-id="626dd-117">PARAMETERS</span></span>

### <span data-ttu-id="626dd-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="626dd-118">-Azure</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="626dd-119">-DefaultProfile</span></span>
<span data-ttu-id="626dd-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="626dd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="626dd-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="626dd-121">-FailoverDeploymentModel</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626dd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="626dd-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626dd-123">-Path</span><span class="sxs-lookup"><span data-stu-id="626dd-123">-Path</span></span>
<span data-ttu-id="626dd-124">指定復原方案檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="626dd-124">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626dd-125">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="626dd-125">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626dd-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="626dd-126">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626dd-127">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="626dd-127">-PrimarySite</span></span>
```yaml
Type: ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626dd-128">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="626dd-128">-ProtectionEntityList</span></span>
```yaml
Type: ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="626dd-129">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="626dd-129">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626dd-130">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="626dd-130">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626dd-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="626dd-131">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="626dd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="626dd-132">CommonParameters</span></span>
<span data-ttu-id="626dd-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="626dd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="626dd-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="626dd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="626dd-135">輸入</span><span class="sxs-lookup"><span data-stu-id="626dd-135">INPUTS</span></span>

### <span data-ttu-id="626dd-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="626dd-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="626dd-137">形參 "ProtectionEntityList" 接受管線中 "ASRProtectionEntity [] 類型的值</span><span class="sxs-lookup"><span data-stu-id="626dd-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="626dd-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="626dd-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="626dd-139">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem [] 類型的值</span><span class="sxs-lookup"><span data-stu-id="626dd-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="626dd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="626dd-140">OUTPUTS</span></span>

## <span data-ttu-id="626dd-141">筆記</span><span class="sxs-lookup"><span data-stu-id="626dd-141">NOTES</span></span>

## <span data-ttu-id="626dd-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="626dd-142">RELATED LINKS</span></span>

[<span data-ttu-id="626dd-143">AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="626dd-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="626dd-144">移除-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="626dd-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="626dd-145">更新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="626dd-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


