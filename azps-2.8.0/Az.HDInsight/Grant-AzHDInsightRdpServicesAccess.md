---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 6cbe18311f4a14b31bc50f7c0b95266bf99d4a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612303"
---
# <span data-ttu-id="cffb0-101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cffb0-101">Grant-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="cffb0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cffb0-102">SYNOPSIS</span></span>
<span data-ttu-id="cffb0-103">授與 Windows 群集的 RDP 存取權。</span><span class="sxs-lookup"><span data-stu-id="cffb0-103">Grants RDP access to the Windows cluster.</span></span>

## <span data-ttu-id="cffb0-104">句法</span><span class="sxs-lookup"><span data-stu-id="cffb0-104">SYNTAX</span></span>

```
Grant-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cffb0-105">說明</span><span class="sxs-lookup"><span data-stu-id="cffb0-105">DESCRIPTION</span></span>
<span data-ttu-id="cffb0-106">**Grant AzHDInsightRdpServicesAccess** Cmdlet 會啟用遠端桌面通訊協定 (RDP) 來存取 Windows 的 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="cffb0-106">The **Grant-AzHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="cffb0-107">示例</span><span class="sxs-lookup"><span data-stu-id="cffb0-107">EXAMPLES</span></span>

### <span data-ttu-id="cffb0-108">範例1：向 Azure HDInsight 群集授與 RDP 存取權</span><span class="sxs-lookup"><span data-stu-id="cffb0-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="cffb0-109">這個命令會將 RDP 存取權授予名為-hadoop-001 的群集。</span><span class="sxs-lookup"><span data-stu-id="cffb0-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="cffb0-110">參數</span><span class="sxs-lookup"><span data-stu-id="cffb0-110">PARAMETERS</span></span>

### <span data-ttu-id="cffb0-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cffb0-111">-ClusterName</span></span>
<span data-ttu-id="cffb0-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="cffb0-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="cffb0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cffb0-113">-DefaultProfile</span></span>
<span data-ttu-id="cffb0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cffb0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cffb0-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="cffb0-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="cffb0-116">指定有效期（作為 **DateTime** 物件），用於 RDP 存取群集。</span><span class="sxs-lookup"><span data-stu-id="cffb0-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffb0-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="cffb0-117">-RdpCredential</span></span>
<span data-ttu-id="cffb0-118">指定群集的 RDP 認證。</span><span class="sxs-lookup"><span data-stu-id="cffb0-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="cffb0-119">這只適用于 Windows 群集。</span><span class="sxs-lookup"><span data-stu-id="cffb0-119">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="cffb0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cffb0-120">-ResourceGroupName</span></span>
<span data-ttu-id="cffb0-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cffb0-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cffb0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffb0-122">CommonParameters</span></span>
<span data-ttu-id="cffb0-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cffb0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffb0-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cffb0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffb0-125">輸入</span><span class="sxs-lookup"><span data-stu-id="cffb0-125">INPUTS</span></span>

### <span data-ttu-id="cffb0-126">所有</span><span class="sxs-lookup"><span data-stu-id="cffb0-126">None</span></span>

## <span data-ttu-id="cffb0-127">輸出</span><span class="sxs-lookup"><span data-stu-id="cffb0-127">OUTPUTS</span></span>

### <span data-ttu-id="cffb0-128">System.void</span><span class="sxs-lookup"><span data-stu-id="cffb0-128">System.Void</span></span>

## <span data-ttu-id="cffb0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="cffb0-129">NOTES</span></span>

## <span data-ttu-id="cffb0-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="cffb0-130">RELATED LINKS</span></span>

[<span data-ttu-id="cffb0-131">吊銷-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cffb0-131">Revoke-AzHDInsightRdpServicesAccess</span></span>](./Revoke-AzHDInsightRdpServicesAccess.md)


