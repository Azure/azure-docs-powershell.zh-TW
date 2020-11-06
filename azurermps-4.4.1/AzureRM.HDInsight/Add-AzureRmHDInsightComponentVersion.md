---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightComponentVersion.md
ms.openlocfilehash: 300244048ae6855c7c621f9950677c985dcb78cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457596"
---
# <span data-ttu-id="01cdc-101">Add-AzureRmHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="01cdc-101">Add-AzureRmHDInsightComponentVersion</span></span>

## <span data-ttu-id="01cdc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="01cdc-103">將在群集中執行的服務的版本新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="01cdc-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01cdc-104">句法</span><span class="sxs-lookup"><span data-stu-id="01cdc-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01cdc-105">說明</span><span class="sxs-lookup"><span data-stu-id="01cdc-105">DESCRIPTION</span></span>
<span data-ttu-id="01cdc-106">Add-AzureRmHDInsightComponentVersion Cmdlet 會將在群集中執行的服務版本新增到由 New-AzureRmHDInsightClusterConfig Cmdlet 建立的 Azure HDInsight 設定物件。</span><span class="sxs-lookup"><span data-stu-id="01cdc-106">The Add-AzureRmHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="01cdc-107">示例</span><span class="sxs-lookup"><span data-stu-id="01cdc-107">EXAMPLES</span></span>

### <span data-ttu-id="01cdc-108">--------------------------範例1：將 Spark 的版本新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="01cdc-108">--------------------------  Example 1: Add a version for Spark to the cluster configuration object.</span></span>  --------------------------
<span data-ttu-id="01cdc-109">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="01cdc-109">@{paragraph=PS C:\\\>}</span></span>







```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container001"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-spark-001"
        $clusterCreds = Get-Credential
        $sshClusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzureRmHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="01cdc-110">這個命令會將 Spark 版本新增到名為「您的 Spark-001」的 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="01cdc-110">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="01cdc-111">參數</span><span class="sxs-lookup"><span data-stu-id="01cdc-111">PARAMETERS</span></span>

### <span data-ttu-id="01cdc-112">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="01cdc-112">-ComponentName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cdc-113">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="01cdc-113">-ComponentVersion</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cdc-114">-Config</span><span class="sxs-lookup"><span data-stu-id="01cdc-114">-Config</span></span>
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

### <span data-ttu-id="01cdc-115">-確認</span><span class="sxs-lookup"><span data-stu-id="01cdc-115">-Confirm</span></span>
<span data-ttu-id="01cdc-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="01cdc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01cdc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01cdc-117">-WhatIf</span></span>
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

### <span data-ttu-id="01cdc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01cdc-118">-DefaultProfile</span></span>
<span data-ttu-id="01cdc-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="01cdc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01cdc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01cdc-120">CommonParameters</span></span>
<span data-ttu-id="01cdc-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01cdc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01cdc-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="01cdc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01cdc-123">輸入</span><span class="sxs-lookup"><span data-stu-id="01cdc-123">INPUTS</span></span>

### <span data-ttu-id="01cdc-124">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="01cdc-124">AzureHDInsightConfig</span></span>
<span data-ttu-id="01cdc-125">形參 "Config" 接受管線中 "AzureHDInsightConfig" 類型的值</span><span class="sxs-lookup"><span data-stu-id="01cdc-125">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="01cdc-126">輸出</span><span class="sxs-lookup"><span data-stu-id="01cdc-126">OUTPUTS</span></span>

### <span data-ttu-id="01cdc-127">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="01cdc-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="01cdc-128">筆記</span><span class="sxs-lookup"><span data-stu-id="01cdc-128">NOTES</span></span>

## <span data-ttu-id="01cdc-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="01cdc-129">RELATED LINKS</span></span>
