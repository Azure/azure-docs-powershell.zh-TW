---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: fc992b427e0c07b1f9db634f9369c21917ec9556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626624"
---
# <span data-ttu-id="f3450-101">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="f3450-101">Add-AzureRmHDInsightClusterIdentity</span></span>

## <span data-ttu-id="f3450-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3450-102">SYNOPSIS</span></span>
<span data-ttu-id="f3450-103">將群集身分識別新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="f3450-103">Adds a cluster identity to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3450-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3450-104">SYNTAX</span></span>

### <span data-ttu-id="f3450-105">CertificateFilePath (預設) </span><span class="sxs-lookup"><span data-stu-id="f3450-105">CertificateFilePath (Default)</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3450-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f3450-106">CertificateFileContents</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3450-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3450-107">DESCRIPTION</span></span>
<span data-ttu-id="f3450-108">**AzureRmHDInsightClusterIdentity** Cmdlet 會將群集身分識別新增至由 New-AzureRmHDInsightClusterConfig Cmdlet 建立的 Azure HDInsight 設定物件。</span><span class="sxs-lookup"><span data-stu-id="f3450-108">The **Add-AzureRmHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="f3450-109">示例</span><span class="sxs-lookup"><span data-stu-id="f3450-109">EXAMPLES</span></span>

### <span data-ttu-id="f3450-110">範例1：將 [群集身分識別資訊] 新增到 [群集設定] 物件</span><span class="sxs-lookup"><span data-stu-id="f3450-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzureRmContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="f3450-111">這個命令會將群集身分識別資訊新增到名為 [hadoop-001] 的群集中，讓群集能夠存取 Azure Data Lake Store。</span><span class="sxs-lookup"><span data-stu-id="f3450-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="f3450-112">參數</span><span class="sxs-lookup"><span data-stu-id="f3450-112">PARAMETERS</span></span>

### <span data-ttu-id="f3450-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="f3450-113">-AadTenantId</span></span>
<span data-ttu-id="f3450-114">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3450-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f3450-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f3450-115">-CertificateFileContents</span></span>
<span data-ttu-id="f3450-116">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="f3450-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f3450-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f3450-117">-CertificateFilePath</span></span>
<span data-ttu-id="f3450-118">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="f3450-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f3450-119">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="f3450-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f3450-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f3450-120">-CertificatePassword</span></span>
<span data-ttu-id="f3450-121">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="f3450-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f3450-122">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="f3450-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f3450-123">-Config</span><span class="sxs-lookup"><span data-stu-id="f3450-123">-Config</span></span>
<span data-ttu-id="f3450-124">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="f3450-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="f3450-125">這個物件是由 New-AzureRmHDInsightClusterConfig Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="f3450-125">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="f3450-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f3450-126">-ObjectId</span></span>
<span data-ttu-id="f3450-127">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="f3450-127">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="f3450-128">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="f3450-128">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f3450-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3450-129">-DefaultProfile</span></span>
<span data-ttu-id="f3450-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3450-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3450-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3450-131">CommonParameters</span></span>
<span data-ttu-id="f3450-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3450-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3450-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3450-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3450-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f3450-134">INPUTS</span></span>

### <span data-ttu-id="f3450-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f3450-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="f3450-136">形參 "Config" 接受管線中 "AzureHDInsightConfig" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f3450-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

### <span data-ttu-id="f3450-137">Guid</span><span class="sxs-lookup"><span data-stu-id="f3450-137">Guid</span></span>
<span data-ttu-id="f3450-138">形參 "ObjectId" 接受管線中類型 "Guid" 的值</span><span class="sxs-lookup"><span data-stu-id="f3450-138">Parameter 'ObjectId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="f3450-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f3450-139">OUTPUTS</span></span>

### <span data-ttu-id="f3450-140">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f3450-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f3450-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f3450-141">NOTES</span></span>

## <span data-ttu-id="f3450-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3450-142">RELATED LINKS</span></span>

[<span data-ttu-id="f3450-143">新-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f3450-143">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


