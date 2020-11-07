---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: ddc269d342a6119187ec578e236a30c928d9ea3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787633"
---
# <span data-ttu-id="c34ce-101">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c34ce-101">Revoke-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="c34ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c34ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c34ce-103">停用 HTTP 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="c34ce-103">Disables HTTP access to the cluster.</span></span>

## <span data-ttu-id="c34ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="c34ce-104">SYNTAX</span></span>

```
Revoke-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c34ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="c34ce-105">DESCRIPTION</span></span>
<span data-ttu-id="c34ce-106">**AzHDInsightHttpServicesAccess** Cmdlet 會針對 ODBC、Ambari、Oozie 和 webHCatalog web 服務，停用 Azure HDInsight 群集的 HTTP 存取。</span><span class="sxs-lookup"><span data-stu-id="c34ce-106">The **Revoke-AzHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="c34ce-107">示例</span><span class="sxs-lookup"><span data-stu-id="c34ce-107">EXAMPLES</span></span>

### <span data-ttu-id="c34ce-108">範例1：停用 HTTP 存取群集</span><span class="sxs-lookup"><span data-stu-id="c34ce-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="c34ce-109">這個命令會撤銷名為 hadoop_001 的群集的 HTTP 存取權。</span><span class="sxs-lookup"><span data-stu-id="c34ce-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="c34ce-110">參數</span><span class="sxs-lookup"><span data-stu-id="c34ce-110">PARAMETERS</span></span>

### <span data-ttu-id="c34ce-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c34ce-111">-ClusterName</span></span>
<span data-ttu-id="c34ce-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c34ce-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c34ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c34ce-113">-DefaultProfile</span></span>
<span data-ttu-id="c34ce-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c34ce-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c34ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c34ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="c34ce-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c34ce-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c34ce-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34ce-117">CommonParameters</span></span>
<span data-ttu-id="c34ce-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c34ce-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34ce-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c34ce-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34ce-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c34ce-120">INPUTS</span></span>

### <span data-ttu-id="c34ce-121">所有</span><span class="sxs-lookup"><span data-stu-id="c34ce-121">None</span></span>

## <span data-ttu-id="c34ce-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c34ce-122">OUTPUTS</span></span>

### <span data-ttu-id="c34ce-123">HttpConnectivitySettings 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="c34ce-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="c34ce-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c34ce-124">NOTES</span></span>

## <span data-ttu-id="c34ce-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c34ce-125">RELATED LINKS</span></span>

[<span data-ttu-id="c34ce-126">授與 AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c34ce-126">Grant-AzHDInsightHttpServicesAccess</span></span>](./Grant-AzHDInsightHttpServicesAccess.md)


