---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285515"
---
# <span data-ttu-id="0402f-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="0402f-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="0402f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0402f-102">SYNOPSIS</span></span>
<span data-ttu-id="0402f-103">Test-AzStackHCIConnection 驗證來自內部部署叢集節點的連線至 Azure 堆疊 HCI 所需的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="0402f-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="0402f-104">句法</span><span class="sxs-lookup"><span data-stu-id="0402f-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="0402f-105">說明</span><span class="sxs-lookup"><span data-stu-id="0402f-105">DESCRIPTION</span></span>
<span data-ttu-id="0402f-106">Test-AzStackHCIConnection 驗證來自內部部署叢集節點的連線至 Azure 堆疊 HCI 所需的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="0402f-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="0402f-107">示例</span><span class="sxs-lookup"><span data-stu-id="0402f-107">EXAMPLES</span></span>

### <span data-ttu-id="0402f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0402f-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node. Success case.
```

<span data-ttu-id="0402f-109">C:\PS \> 測試-AzStackHCIConnection test：連線至 Azure 堆疊 HCI Service EndpointTested： https://azurestackhci-df.azurefd.net/health IsRequired： True 結果： Succeeded</span><span class="sxs-lookup"><span data-stu-id="0402f-109">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded</span></span>

### <span data-ttu-id="0402f-110">範例2</span><span class="sxs-lookup"><span data-stu-id="0402f-110">EXAMPLE 2</span></span>
```
Invoking on one of the cluster node. Failed case.
```

<span data-ttu-id="0402f-111">C:\PS \> 測試-AzStackHCIConnection test：連線至 Azure 堆疊 HCI Service EndpointTested： https://azurestackhci-df.azurefd.net/health IsRequired： True 結果：失敗的 FailedNodes： Node1inClus2、Node2inClus3</span><span class="sxs-lookup"><span data-stu-id="0402f-111">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span></span>

## <span data-ttu-id="0402f-112">參數</span><span class="sxs-lookup"><span data-stu-id="0402f-112">PARAMETERS</span></span>

### <span data-ttu-id="0402f-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="0402f-113">-ComputerName</span></span>
<span data-ttu-id="0402f-114">指定登錄至 Azure 之內部部署群集中的其中一個叢集節點。</span><span class="sxs-lookup"><span data-stu-id="0402f-114">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0402f-115">-認證</span><span class="sxs-lookup"><span data-stu-id="0402f-115">-Credential</span></span>
<span data-ttu-id="0402f-116">指定 ComputerName 的認證。</span><span class="sxs-lookup"><span data-stu-id="0402f-116">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="0402f-117">[預設值] 是執行 Cmdlet 的目前使用者。</span><span class="sxs-lookup"><span data-stu-id="0402f-117">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0402f-118">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="0402f-118">-EnvironmentName</span></span>
<span data-ttu-id="0402f-119">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="0402f-119">Specifies the Azure Environment.</span></span>
<span data-ttu-id="0402f-120">預設值為 AzureCloud。</span><span class="sxs-lookup"><span data-stu-id="0402f-120">Default is AzureCloud.</span></span>
<span data-ttu-id="0402f-121">有效值為 AzureCloud、AzureChinaCloud、AzureUSGovernment、AzureGermanCloud、AzurePPE</span><span class="sxs-lookup"><span data-stu-id="0402f-121">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0402f-122">-Region</span><span class="sxs-lookup"><span data-stu-id="0402f-122">-Region</span></span>
<span data-ttu-id="0402f-123">指定要連接的地區。</span><span class="sxs-lookup"><span data-stu-id="0402f-123">Specifies the Region to connect to.</span></span>
<span data-ttu-id="0402f-124">除非是 [無中的區域]，否則不使用。</span><span class="sxs-lookup"><span data-stu-id="0402f-124">Not used unless it is Canary region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0402f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0402f-125">CommonParameters</span></span>
<span data-ttu-id="0402f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0402f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0402f-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0402f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0402f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0402f-128">INPUTS</span></span>

## <span data-ttu-id="0402f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0402f-129">OUTPUTS</span></span>

### <span data-ttu-id="0402f-130">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="0402f-130">PSCustomObject.</span></span> <span data-ttu-id="0402f-131">在 PSCustomObject 中傳回下列屬性</span><span class="sxs-lookup"><span data-stu-id="0402f-131">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="0402f-132">測試：執行的測試名稱。</span><span class="sxs-lookup"><span data-stu-id="0402f-132">Test: Name of the test performed.</span></span>
### <span data-ttu-id="0402f-133">EndpointTested：測試中使用的端點。</span><span class="sxs-lookup"><span data-stu-id="0402f-133">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="0402f-134">IsRequired： True 或 False</span><span class="sxs-lookup"><span data-stu-id="0402f-134">IsRequired: True or False</span></span>
### <span data-ttu-id="0402f-135">結果：成功或失敗</span><span class="sxs-lookup"><span data-stu-id="0402f-135">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="0402f-136">FailedNodes：測試失敗的節點清單。</span><span class="sxs-lookup"><span data-stu-id="0402f-136">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="0402f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0402f-137">NOTES</span></span>

## <span data-ttu-id="0402f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0402f-138">RELATED LINKS</span></span>
