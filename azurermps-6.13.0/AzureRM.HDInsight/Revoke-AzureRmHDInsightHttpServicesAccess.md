---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 93024e0719687c10ec07daa7269d742db012abe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455344"
---
# <span data-ttu-id="7a0fc-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7a0fc-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="7a0fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0fc-103">停用 HTTP 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="7a0fc-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a0fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a0fc-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a0fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="7a0fc-105">DESCRIPTION</span></span>
<span data-ttu-id="7a0fc-106">**AzureRmHDInsightHttpServicesAccess** Cmdlet 會針對 ODBC、Ambari、Oozie 和 webHCatalog web 服務，停用 Azure HDInsight 群集的 HTTP 存取。</span><span class="sxs-lookup"><span data-stu-id="7a0fc-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="7a0fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="7a0fc-107">EXAMPLES</span></span>

### <span data-ttu-id="7a0fc-108">範例1：停用 HTTP 存取群集</span><span class="sxs-lookup"><span data-stu-id="7a0fc-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="7a0fc-109">這個命令會撤銷名為 hadoop_001 的群集的 HTTP 存取權。</span><span class="sxs-lookup"><span data-stu-id="7a0fc-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="7a0fc-110">參數</span><span class="sxs-lookup"><span data-stu-id="7a0fc-110">PARAMETERS</span></span>

### <span data-ttu-id="7a0fc-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7a0fc-111">-ClusterName</span></span>
<span data-ttu-id="7a0fc-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a0fc-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="7a0fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0fc-113">-DefaultProfile</span></span>
<span data-ttu-id="7a0fc-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7a0fc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a0fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a0fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a0fc-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a0fc-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7a0fc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0fc-117">CommonParameters</span></span>
<span data-ttu-id="7a0fc-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a0fc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0fc-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7a0fc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0fc-120">輸入</span><span class="sxs-lookup"><span data-stu-id="7a0fc-120">INPUTS</span></span>

### <span data-ttu-id="7a0fc-121">所有</span><span class="sxs-lookup"><span data-stu-id="7a0fc-121">None</span></span>

## <span data-ttu-id="7a0fc-122">輸出</span><span class="sxs-lookup"><span data-stu-id="7a0fc-122">OUTPUTS</span></span>

### <span data-ttu-id="7a0fc-123">HttpConnectivitySettings 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="7a0fc-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="7a0fc-124">筆記</span><span class="sxs-lookup"><span data-stu-id="7a0fc-124">NOTES</span></span>

## <span data-ttu-id="7a0fc-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a0fc-125">RELATED LINKS</span></span>

[<span data-ttu-id="7a0fc-126">授與 AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7a0fc-126">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)


