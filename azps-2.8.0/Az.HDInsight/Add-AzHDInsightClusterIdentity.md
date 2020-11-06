---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 035b21684c3d8fc64cee7ee78b7b4cb2adf21f01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612329"
---
# <span data-ttu-id="99f08-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="99f08-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="99f08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99f08-102">SYNOPSIS</span></span>
<span data-ttu-id="99f08-103">將群集身分識別新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="99f08-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="99f08-104">句法</span><span class="sxs-lookup"><span data-stu-id="99f08-104">SYNTAX</span></span>

### <span data-ttu-id="99f08-105">CertificateFilePath (預設) </span><span class="sxs-lookup"><span data-stu-id="99f08-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99f08-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="99f08-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99f08-107">說明</span><span class="sxs-lookup"><span data-stu-id="99f08-107">DESCRIPTION</span></span>
<span data-ttu-id="99f08-108">**AzHDInsightClusterIdentity** Cmdlet 會將群集身分識別新增至由 New-AzHDInsightClusterConfig Cmdlet 建立的 Azure HDInsight 設定物件。</span><span class="sxs-lookup"><span data-stu-id="99f08-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="99f08-109">示例</span><span class="sxs-lookup"><span data-stu-id="99f08-109">EXAMPLES</span></span>

### <span data-ttu-id="99f08-110">範例1：將 [群集身分識別資訊] 新增到 [群集設定] 物件</span><span class="sxs-lookup"><span data-stu-id="99f08-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="99f08-111">這個命令會將群集身分識別資訊新增到名為 [hadoop-001] 的群集中，讓群集能夠存取 Azure Data Lake Store。</span><span class="sxs-lookup"><span data-stu-id="99f08-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="99f08-112">參數</span><span class="sxs-lookup"><span data-stu-id="99f08-112">PARAMETERS</span></span>

### <span data-ttu-id="99f08-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="99f08-113">-AadTenantId</span></span>
<span data-ttu-id="99f08-114">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="99f08-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="99f08-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="99f08-115">-CertificateFileContents</span></span>
<span data-ttu-id="99f08-116">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="99f08-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="99f08-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="99f08-117">-CertificateFilePath</span></span>
<span data-ttu-id="99f08-118">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="99f08-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="99f08-119">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="99f08-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="99f08-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="99f08-120">-CertificatePassword</span></span>
<span data-ttu-id="99f08-121">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="99f08-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="99f08-122">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="99f08-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="99f08-123">-Config</span><span class="sxs-lookup"><span data-stu-id="99f08-123">-Config</span></span>
<span data-ttu-id="99f08-124">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="99f08-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="99f08-125">這個物件是由 New-AzHDInsightClusterConfig Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="99f08-125">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="99f08-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f08-126">-DefaultProfile</span></span>
<span data-ttu-id="99f08-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="99f08-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99f08-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="99f08-128">-ObjectId</span></span>
<span data-ttu-id="99f08-129">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="99f08-129">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="99f08-130">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="99f08-130">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="99f08-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f08-131">CommonParameters</span></span>
<span data-ttu-id="99f08-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99f08-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f08-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99f08-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f08-134">輸入</span><span class="sxs-lookup"><span data-stu-id="99f08-134">INPUTS</span></span>

### <span data-ttu-id="99f08-135">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="99f08-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="99f08-136">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="99f08-136">System.Guid</span></span>

## <span data-ttu-id="99f08-137">輸出</span><span class="sxs-lookup"><span data-stu-id="99f08-137">OUTPUTS</span></span>

### <span data-ttu-id="99f08-138">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="99f08-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="99f08-139">筆記</span><span class="sxs-lookup"><span data-stu-id="99f08-139">NOTES</span></span>

## <span data-ttu-id="99f08-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="99f08-140">RELATED LINKS</span></span>

[<span data-ttu-id="99f08-141">新-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="99f08-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


