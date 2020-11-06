---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 7f5fcb8dcfbb325b8bc0381b3c943e550fe27e62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612274"
---
# <span data-ttu-id="6ad56-101">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6ad56-101">Revoke-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="6ad56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ad56-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad56-103">停用 RDP 對 Windows 群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="6ad56-103">Disables RDP access to a Windows cluster.</span></span>

## <span data-ttu-id="6ad56-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ad56-104">SYNTAX</span></span>

```
Revoke-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ad56-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ad56-105">DESCRIPTION</span></span>
<span data-ttu-id="6ad56-106">**AzHDInsightRdpServicesAccess** Cmdlet 會停用遠端桌面通訊協定 (RDP) 存取 Windows 基礎的 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="6ad56-106">The **Revoke-AzHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6ad56-107">示例</span><span class="sxs-lookup"><span data-stu-id="6ad56-107">EXAMPLES</span></span>

### <span data-ttu-id="6ad56-108">範例1：停用 RDP 存取特定的群集</span><span class="sxs-lookup"><span data-stu-id="6ad56-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="6ad56-109">這個命令會撤銷名為-hadoop-001 之群集的 RDP 存取權。</span><span class="sxs-lookup"><span data-stu-id="6ad56-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6ad56-110">參數</span><span class="sxs-lookup"><span data-stu-id="6ad56-110">PARAMETERS</span></span>

### <span data-ttu-id="6ad56-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6ad56-111">-ClusterName</span></span>
<span data-ttu-id="6ad56-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ad56-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6ad56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad56-113">-DefaultProfile</span></span>
<span data-ttu-id="6ad56-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6ad56-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ad56-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad56-115">-ResourceGroupName</span></span>
<span data-ttu-id="6ad56-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ad56-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6ad56-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad56-117">CommonParameters</span></span>
<span data-ttu-id="6ad56-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ad56-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad56-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ad56-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad56-120">輸入</span><span class="sxs-lookup"><span data-stu-id="6ad56-120">INPUTS</span></span>

### <span data-ttu-id="6ad56-121">所有</span><span class="sxs-lookup"><span data-stu-id="6ad56-121">None</span></span>

## <span data-ttu-id="6ad56-122">輸出</span><span class="sxs-lookup"><span data-stu-id="6ad56-122">OUTPUTS</span></span>

### <span data-ttu-id="6ad56-123">System.void</span><span class="sxs-lookup"><span data-stu-id="6ad56-123">System.Void</span></span>

## <span data-ttu-id="6ad56-124">筆記</span><span class="sxs-lookup"><span data-stu-id="6ad56-124">NOTES</span></span>

## <span data-ttu-id="6ad56-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ad56-125">RELATED LINKS</span></span>

[<span data-ttu-id="6ad56-126">授與 AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6ad56-126">Grant-AzHDInsightRdpServicesAccess</span></span>](./Grant-AzHDInsightRdpServicesAccess.md)


