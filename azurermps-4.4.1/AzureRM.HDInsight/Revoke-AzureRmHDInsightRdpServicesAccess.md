---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: f05cae3484067f227fde8f30cd7806307832b185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446806"
---
# <span data-ttu-id="30cb2-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="30cb2-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="30cb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="30cb2-103">停用 RDP 對 Windows 群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="30cb2-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30cb2-104">句法</span><span class="sxs-lookup"><span data-stu-id="30cb2-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30cb2-105">說明</span><span class="sxs-lookup"><span data-stu-id="30cb2-105">DESCRIPTION</span></span>
<span data-ttu-id="30cb2-106">**AzureRmHDInsightRdpServicesAccess** Cmdlet 會停用遠端桌面通訊協定 (RDP) 存取 Windows 基礎的 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="30cb2-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="30cb2-107">示例</span><span class="sxs-lookup"><span data-stu-id="30cb2-107">EXAMPLES</span></span>

### <span data-ttu-id="30cb2-108">範例1：停用 RDP 存取特定的群集</span><span class="sxs-lookup"><span data-stu-id="30cb2-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="30cb2-109">這個命令會撤銷名為-hadoop-001 之群集的 RDP 存取權。</span><span class="sxs-lookup"><span data-stu-id="30cb2-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="30cb2-110">參數</span><span class="sxs-lookup"><span data-stu-id="30cb2-110">PARAMETERS</span></span>

### <span data-ttu-id="30cb2-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="30cb2-111">-ClusterName</span></span>
<span data-ttu-id="30cb2-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="30cb2-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="30cb2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30cb2-113">-ResourceGroupName</span></span>
<span data-ttu-id="30cb2-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="30cb2-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="30cb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30cb2-115">-DefaultProfile</span></span>
<span data-ttu-id="30cb2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30cb2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30cb2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30cb2-117">CommonParameters</span></span>
<span data-ttu-id="30cb2-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30cb2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30cb2-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30cb2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30cb2-120">輸入</span><span class="sxs-lookup"><span data-stu-id="30cb2-120">INPUTS</span></span>

## <span data-ttu-id="30cb2-121">輸出</span><span class="sxs-lookup"><span data-stu-id="30cb2-121">OUTPUTS</span></span>

### <span data-ttu-id="30cb2-122">System.void</span><span class="sxs-lookup"><span data-stu-id="30cb2-122">System.Void</span></span>

## <span data-ttu-id="30cb2-123">筆記</span><span class="sxs-lookup"><span data-stu-id="30cb2-123">NOTES</span></span>

## <span data-ttu-id="30cb2-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="30cb2-124">RELATED LINKS</span></span>

[<span data-ttu-id="30cb2-125">授與 AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="30cb2-125">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


