---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c44fea946f98c6ac19e77e7012910afac37bff7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278526"
---
# <span data-ttu-id="3279d-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="3279d-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="3279d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3279d-102">SYNOPSIS</span></span>
<span data-ttu-id="3279d-103">新增安全設定檔至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="3279d-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="3279d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3279d-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -DomainResourceId <String>
 -DomainUserCredential <PSCredential> [-OrganizationalUnitDN <String>] -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3279d-105">說明</span><span class="sxs-lookup"><span data-stu-id="3279d-105">DESCRIPTION</span></span>
<span data-ttu-id="3279d-106">安全設定檔是透過 kerberizing 來建立安全的群集。</span><span class="sxs-lookup"><span data-stu-id="3279d-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="3279d-107">安全性設定檔包含將群集加入 Active Directory 網域的相關設定。</span><span class="sxs-lookup"><span data-stu-id="3279d-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="3279d-108">示例</span><span class="sxs-lookup"><span data-stu-id="3279d-108">EXAMPLES</span></span>

### <span data-ttu-id="3279d-109">範例1：將安全性設定檔新增至群集設定物件</span><span class="sxs-lookup"><span data-stu-id="3279d-109">Example 1: Add security profile to the cluster configuration object</span></span>
```
PS C:\> #Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

#Security profile info
PS C:\> $domain="sampledomain.onmicrosoft.com"
PS C:\> $domainUser="sample.user@sampledomain.onmicrosoft.com"
PS C:\> $domainPassword=ConvertTo-SecureString "domainPassword" -AsPlainText -Force
PS C:\> $domainUserCredential=New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
PS C:\> $organizationalUnitDN="ou=testunitdn"
PS C:\> $ldapsUrls=("ldaps://sampledomain.onmicrosoft.com:636","ldaps://sampledomain.onmicrosoft.com:389")
PS C:\> $clusterUsersGroupDNs=("groupdn1","groupdn2")

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightSecurityProfile `
                -Domain $domain `
                -DomainUserCredential $domainUserCredential `
                -OrganizationalUnitDN $organizationalUnitDN `
                -LdapsUrls $ldapsUrls `
                -ClusterUsersGroupDNs $clusterUsersGroupDNs `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="3279d-110">這個命令會將一個安全設定檔值新增到名為 [您的 hadoop-001] 的群集中。</span><span class="sxs-lookup"><span data-stu-id="3279d-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="3279d-111">參數</span><span class="sxs-lookup"><span data-stu-id="3279d-111">PARAMETERS</span></span>

### <span data-ttu-id="3279d-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="3279d-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="3279d-113">將可在 Ambari 和 Ranger 中使用之 Active Directory 群組的可分辨名稱</span><span class="sxs-lookup"><span data-stu-id="3279d-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3279d-114">-Config</span><span class="sxs-lookup"><span data-stu-id="3279d-114">-Config</span></span>
<span data-ttu-id="3279d-115">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="3279d-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3279d-116">這個物件是由 New-AzHDInsightClusterConfig Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="3279d-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3279d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3279d-117">-DefaultProfile</span></span>
<span data-ttu-id="3279d-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3279d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3279d-119">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="3279d-119">-DomainResourceId</span></span>
<span data-ttu-id="3279d-120">群集的 Active Directory 網域資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3279d-120">Active Directory domain resource id for the cluster.</span></span>

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

### <span data-ttu-id="3279d-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="3279d-121">-DomainUserCredential</span></span>
<span data-ttu-id="3279d-122">具有足夠許可權的網域使用者帳號憑證來建立群集。</span><span class="sxs-lookup"><span data-stu-id="3279d-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="3279d-123">[使用者名] 應為 [ user@domain 格式]</span><span class="sxs-lookup"><span data-stu-id="3279d-123">Username should be in user@domain format</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3279d-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="3279d-124">-LdapsUrls</span></span>
<span data-ttu-id="3279d-125">Active Directory 的一或多個 LDAPS 伺服器的 url</span><span class="sxs-lookup"><span data-stu-id="3279d-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3279d-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="3279d-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="3279d-127">在 Active directory 中將會建立使用者和電腦帳戶的組織單位的可分辨名稱</span><span class="sxs-lookup"><span data-stu-id="3279d-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="3279d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="3279d-128">-Confirm</span></span>
<span data-ttu-id="3279d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3279d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3279d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3279d-130">-WhatIf</span></span>
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

### <span data-ttu-id="3279d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3279d-131">CommonParameters</span></span>
<span data-ttu-id="3279d-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3279d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3279d-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3279d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3279d-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3279d-134">INPUTS</span></span>

### <span data-ttu-id="3279d-135">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="3279d-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="3279d-136">輸出</span><span class="sxs-lookup"><span data-stu-id="3279d-136">OUTPUTS</span></span>

### <span data-ttu-id="3279d-137">AzureHDInsightSecurityProfile （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="3279d-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="3279d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3279d-138">NOTES</span></span>

## <span data-ttu-id="3279d-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="3279d-139">RELATED LINKS</span></span>
