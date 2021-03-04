---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: b154ab0bbcf10c0fb1d68b7634e5e2d1bf97a45d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911678"
---
# <span data-ttu-id="409db-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="409db-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="409db-102">簡介</span><span class="sxs-lookup"><span data-stu-id="409db-102">SYNOPSIS</span></span>
<span data-ttu-id="409db-103">新增組群身分識別至組組物件。</span><span class="sxs-lookup"><span data-stu-id="409db-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="409db-104">語法</span><span class="sxs-lookup"><span data-stu-id="409db-104">SYNTAX</span></span>

### <span data-ttu-id="409db-105">CertificateFilePath (預設) </span><span class="sxs-lookup"><span data-stu-id="409db-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409db-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="409db-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="409db-107">描述</span><span class="sxs-lookup"><span data-stu-id="409db-107">DESCRIPTION</span></span>
<span data-ttu-id="409db-108">**Add-AzHDInsightClusterIdentity** Cmdlet 會將叢集身分識別新增到由 New-AzHDInsightClusterConfig Cmdlet 所建立 Azure HDInsight 組New-AzHDInsightClusterConfig物件。</span><span class="sxs-lookup"><span data-stu-id="409db-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="409db-109">例子</span><span class="sxs-lookup"><span data-stu-id="409db-109">EXAMPLES</span></span>

### <span data-ttu-id="409db-110">範例 1：新增組群身分識別資訊至組組物件</span><span class="sxs-lookup"><span data-stu-id="409db-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
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

# Cluster Identity values
PS C:\> $tenantId = (Get-AzContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $applicationId = "<Azure AD Service Principal Application ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -Application $applicationId
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="409db-111">此命令會將組群身分識別資訊新增到名為 your-hadoop-001 的組集中，讓該組組存取 Azure Data Lake Store。</span><span class="sxs-lookup"><span data-stu-id="409db-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="409db-112">參數</span><span class="sxs-lookup"><span data-stu-id="409db-112">PARAMETERS</span></span>

### <span data-ttu-id="409db-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="409db-113">-AadTenantId</span></span>
<span data-ttu-id="409db-114">指定存取 Azure Data Lake Store 時將會使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="409db-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409db-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="409db-115">-ApplicationId</span></span>
<span data-ttu-id="409db-116">存取 Azure Data Lake 的服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="409db-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409db-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="409db-117">-CertificateFileContents</span></span>
<span data-ttu-id="409db-118">指定存取 Azure Data Lake Store 時將使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="409db-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409db-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="409db-119">-CertificateFilePath</span></span>
<span data-ttu-id="409db-120">指定要用來驗證為服務主體之憑證的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="409db-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="409db-121">當存取 Azure Data Lake Store 時，該組會使用此功能。</span><span class="sxs-lookup"><span data-stu-id="409db-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409db-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="409db-122">-CertificatePassword</span></span>
<span data-ttu-id="409db-123">指定要用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="409db-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="409db-124">當存取 Azure Data Lake Store 時，該組會使用此功能。</span><span class="sxs-lookup"><span data-stu-id="409db-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409db-125">-Config</span><span class="sxs-lookup"><span data-stu-id="409db-125">-Config</span></span>
<span data-ttu-id="409db-126">指定此 Cmdlet 修改的 HDInsight 集區組物件。</span><span class="sxs-lookup"><span data-stu-id="409db-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="409db-127">此物件是由 Cmdlet New-AzHDInsightClusterConfig建立。</span><span class="sxs-lookup"><span data-stu-id="409db-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="409db-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="409db-128">-DefaultProfile</span></span>
<span data-ttu-id="409db-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="409db-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="409db-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="409db-130">-ObjectId</span></span>
<span data-ttu-id="409db-131">指定代表該 (之 Azure AD 服務) GUID 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="409db-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="409db-132">當存取 Azure Data Lake Store 時，該組會使用此功能。</span><span class="sxs-lookup"><span data-stu-id="409db-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="409db-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409db-133">CommonParameters</span></span>
<span data-ttu-id="409db-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="409db-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409db-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="409db-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409db-136">輸入</span><span class="sxs-lookup"><span data-stu-id="409db-136">INPUTS</span></span>

### <span data-ttu-id="409db-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="409db-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="409db-138">System.Guid</span><span class="sxs-lookup"><span data-stu-id="409db-138">System.Guid</span></span>

## <span data-ttu-id="409db-139">輸出</span><span class="sxs-lookup"><span data-stu-id="409db-139">OUTPUTS</span></span>

### <span data-ttu-id="409db-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="409db-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="409db-141">筆記</span><span class="sxs-lookup"><span data-stu-id="409db-141">NOTES</span></span>

## <span data-ttu-id="409db-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="409db-142">RELATED LINKS</span></span>

[<span data-ttu-id="409db-143">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="409db-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


