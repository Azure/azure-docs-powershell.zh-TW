---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: c447d8dbfb7ed0b1fb4cf2ac3ad4c63aa4666ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626293"
---
# <span data-ttu-id="99d16-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="99d16-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="99d16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99d16-102">SYNOPSIS</span></span>
<span data-ttu-id="99d16-103">授權 HTTP 存取群集。</span><span class="sxs-lookup"><span data-stu-id="99d16-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99d16-104">句法</span><span class="sxs-lookup"><span data-stu-id="99d16-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99d16-105">說明</span><span class="sxs-lookup"><span data-stu-id="99d16-105">DESCRIPTION</span></span>
<span data-ttu-id="99d16-106">**授與 AzureRmHDInsightHttpServicesAccess** Cmdlet 會使用 ODBC、Ambari、Oozie 和 web 服務，將 HTTP 存取權授予 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="99d16-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="99d16-107">示例</span><span class="sxs-lookup"><span data-stu-id="99d16-107">EXAMPLES</span></span>

### <span data-ttu-id="99d16-108">範例1：授與 Azure HDInsight 群集的 HTTP 存取權</span><span class="sxs-lookup"><span data-stu-id="99d16-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="99d16-109">這個命令會將 HTTP 存取權授予名為-hadoop-001 的群集。</span><span class="sxs-lookup"><span data-stu-id="99d16-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="99d16-110">參數</span><span class="sxs-lookup"><span data-stu-id="99d16-110">PARAMETERS</span></span>

### <span data-ttu-id="99d16-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="99d16-111">-ClusterName</span></span>
<span data-ttu-id="99d16-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="99d16-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="99d16-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="99d16-113">-HttpCredential</span></span>
<span data-ttu-id="99d16-114">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="99d16-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="99d16-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d16-115">-ResourceGroupName</span></span>
<span data-ttu-id="99d16-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99d16-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="99d16-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d16-117">-DefaultProfile</span></span>
<span data-ttu-id="99d16-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99d16-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99d16-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d16-119">CommonParameters</span></span>
<span data-ttu-id="99d16-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99d16-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d16-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99d16-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d16-122">輸入</span><span class="sxs-lookup"><span data-stu-id="99d16-122">INPUTS</span></span>

## <span data-ttu-id="99d16-123">輸出</span><span class="sxs-lookup"><span data-stu-id="99d16-123">OUTPUTS</span></span>

### <span data-ttu-id="99d16-124">HttpConnectivitySettings 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="99d16-124">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="99d16-125">筆記</span><span class="sxs-lookup"><span data-stu-id="99d16-125">NOTES</span></span>

## <span data-ttu-id="99d16-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="99d16-126">RELATED LINKS</span></span>

[<span data-ttu-id="99d16-127">吊銷-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="99d16-127">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


