---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 644fd5ff1b038f275288e30d85fbc653b6107b1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626411"
---
# <span data-ttu-id="42361-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="42361-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="42361-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42361-102">SYNOPSIS</span></span>
<span data-ttu-id="42361-103">授權 HTTP 存取群集。</span><span class="sxs-lookup"><span data-stu-id="42361-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42361-104">句法</span><span class="sxs-lookup"><span data-stu-id="42361-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42361-105">說明</span><span class="sxs-lookup"><span data-stu-id="42361-105">DESCRIPTION</span></span>
<span data-ttu-id="42361-106">**授與 AzureRmHDInsightHttpServicesAccess** Cmdlet 會使用 ODBC、Ambari、Oozie 和 web 服務，將 HTTP 存取權授予 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="42361-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="42361-107">示例</span><span class="sxs-lookup"><span data-stu-id="42361-107">EXAMPLES</span></span>

### <span data-ttu-id="42361-108">範例1：授與 Azure HDInsight 群集的 HTTP 存取權</span><span class="sxs-lookup"><span data-stu-id="42361-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="42361-109">這個命令會將 HTTP 存取權授予名為-hadoop-001 的群集。</span><span class="sxs-lookup"><span data-stu-id="42361-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="42361-110">參數</span><span class="sxs-lookup"><span data-stu-id="42361-110">PARAMETERS</span></span>

### <span data-ttu-id="42361-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="42361-111">-ClusterName</span></span>
<span data-ttu-id="42361-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="42361-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42361-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42361-113">-DefaultProfile</span></span>
<span data-ttu-id="42361-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="42361-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42361-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="42361-115">-HttpCredential</span></span>
<span data-ttu-id="42361-116">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="42361-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42361-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42361-117">-ResourceGroupName</span></span>
<span data-ttu-id="42361-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="42361-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="42361-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42361-119">CommonParameters</span></span>
<span data-ttu-id="42361-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42361-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42361-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42361-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42361-122">輸入</span><span class="sxs-lookup"><span data-stu-id="42361-122">INPUTS</span></span>

### <span data-ttu-id="42361-123">所有</span><span class="sxs-lookup"><span data-stu-id="42361-123">None</span></span>

## <span data-ttu-id="42361-124">輸出</span><span class="sxs-lookup"><span data-stu-id="42361-124">OUTPUTS</span></span>

### <span data-ttu-id="42361-125">HttpConnectivitySettings 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="42361-125">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="42361-126">筆記</span><span class="sxs-lookup"><span data-stu-id="42361-126">NOTES</span></span>

## <span data-ttu-id="42361-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="42361-127">RELATED LINKS</span></span>

[<span data-ttu-id="42361-128">吊銷-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="42361-128">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


