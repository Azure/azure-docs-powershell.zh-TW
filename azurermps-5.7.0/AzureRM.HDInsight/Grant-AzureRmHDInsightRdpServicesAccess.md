---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 09b389763897f91a23f56f0a3383dd3f7f03ca1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623818"
---
# <span data-ttu-id="983d7-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="983d7-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="983d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="983d7-102">SYNOPSIS</span></span>
<span data-ttu-id="983d7-103">授與 Windows 群集的 RDP 存取權。</span><span class="sxs-lookup"><span data-stu-id="983d7-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="983d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="983d7-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="983d7-105">說明</span><span class="sxs-lookup"><span data-stu-id="983d7-105">DESCRIPTION</span></span>
<span data-ttu-id="983d7-106">**Grant AzureRmHDInsightRdpServicesAccess** Cmdlet 會啟用遠端桌面通訊協定 (RDP) 來存取 Windows 的 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="983d7-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="983d7-107">示例</span><span class="sxs-lookup"><span data-stu-id="983d7-107">EXAMPLES</span></span>

### <span data-ttu-id="983d7-108">範例1：向 Azure HDInsight 群集授與 RDP 存取權</span><span class="sxs-lookup"><span data-stu-id="983d7-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="983d7-109">這個命令會將 RDP 存取權授予名為-hadoop-001 的群集。</span><span class="sxs-lookup"><span data-stu-id="983d7-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="983d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="983d7-110">PARAMETERS</span></span>

### <span data-ttu-id="983d7-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="983d7-111">-ClusterName</span></span>
<span data-ttu-id="983d7-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="983d7-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="983d7-113">-DefaultProfile</span></span>
<span data-ttu-id="983d7-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="983d7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983d7-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="983d7-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="983d7-116">指定有效期（作為 **DateTime** 物件），用於 RDP 存取群集。</span><span class="sxs-lookup"><span data-stu-id="983d7-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983d7-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="983d7-117">-RdpCredential</span></span>
<span data-ttu-id="983d7-118">指定群集的 RDP 認證。</span><span class="sxs-lookup"><span data-stu-id="983d7-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="983d7-119">這只適用于 Windows 群集。</span><span class="sxs-lookup"><span data-stu-id="983d7-119">This is only for Windows clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="983d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="983d7-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="983d7-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="983d7-122">CommonParameters</span></span>
<span data-ttu-id="983d7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="983d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="983d7-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="983d7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="983d7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="983d7-125">INPUTS</span></span>

### <span data-ttu-id="983d7-126">所有</span><span class="sxs-lookup"><span data-stu-id="983d7-126">None</span></span>
<span data-ttu-id="983d7-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="983d7-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="983d7-128">輸出</span><span class="sxs-lookup"><span data-stu-id="983d7-128">OUTPUTS</span></span>

### <span data-ttu-id="983d7-129">System.void</span><span class="sxs-lookup"><span data-stu-id="983d7-129">System.Void</span></span>

## <span data-ttu-id="983d7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="983d7-130">NOTES</span></span>

## <span data-ttu-id="983d7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="983d7-131">RELATED LINKS</span></span>

[<span data-ttu-id="983d7-132">吊銷-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="983d7-132">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


