---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: c531135af3d118a9987a3c328eb4c06847e75fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787678"
---
# <span data-ttu-id="139f2-101">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="139f2-101">Grant-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="139f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="139f2-102">SYNOPSIS</span></span>
<span data-ttu-id="139f2-103">授權 HTTP 存取群集。</span><span class="sxs-lookup"><span data-stu-id="139f2-103">Grants HTTP access to the cluster.</span></span>

## <span data-ttu-id="139f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="139f2-104">SYNTAX</span></span>

```
Grant-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="139f2-105">說明</span><span class="sxs-lookup"><span data-stu-id="139f2-105">DESCRIPTION</span></span>
<span data-ttu-id="139f2-106">**授與 AzHDInsightHttpServicesAccess** Cmdlet 會使用 ODBC、Ambari、Oozie 和 web 服務，將 HTTP 存取權授予 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="139f2-106">The **Grant-AzHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="139f2-107">示例</span><span class="sxs-lookup"><span data-stu-id="139f2-107">EXAMPLES</span></span>

### <span data-ttu-id="139f2-108">範例1：授與 Azure HDInsight 群集的 HTTP 存取權</span><span class="sxs-lookup"><span data-stu-id="139f2-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="139f2-109">這個命令會將 HTTP 存取權授予名為-hadoop-001 的群集。</span><span class="sxs-lookup"><span data-stu-id="139f2-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="139f2-110">參數</span><span class="sxs-lookup"><span data-stu-id="139f2-110">PARAMETERS</span></span>

### <span data-ttu-id="139f2-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="139f2-111">-ClusterName</span></span>
<span data-ttu-id="139f2-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="139f2-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="139f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="139f2-113">-DefaultProfile</span></span>
<span data-ttu-id="139f2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="139f2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="139f2-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="139f2-115">-HttpCredential</span></span>
<span data-ttu-id="139f2-116">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="139f2-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="139f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="139f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="139f2-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="139f2-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="139f2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="139f2-119">CommonParameters</span></span>
<span data-ttu-id="139f2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="139f2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="139f2-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="139f2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="139f2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="139f2-122">INPUTS</span></span>

### <span data-ttu-id="139f2-123">所有</span><span class="sxs-lookup"><span data-stu-id="139f2-123">None</span></span>

## <span data-ttu-id="139f2-124">輸出</span><span class="sxs-lookup"><span data-stu-id="139f2-124">OUTPUTS</span></span>

### <span data-ttu-id="139f2-125">HttpConnectivitySettings 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="139f2-125">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="139f2-126">筆記</span><span class="sxs-lookup"><span data-stu-id="139f2-126">NOTES</span></span>

## <span data-ttu-id="139f2-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="139f2-127">RELATED LINKS</span></span>

[<span data-ttu-id="139f2-128">吊銷-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="139f2-128">Revoke-AzHDInsightHttpServicesAccess</span></span>](./Revoke-AzHDInsightHttpServicesAccess.md)


