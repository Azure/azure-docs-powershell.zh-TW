---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 34831104bc1b27aa115d56545c784e0fea856ba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128147"
---
# <span data-ttu-id="6faed-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="6faed-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="6faed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6faed-102">SYNOPSIS</span></span>
<span data-ttu-id="6faed-103">Test-AzStackHCIConnection 驗證來自內部部署叢集節點的連線至 Azure 堆疊 HCI 所需的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="6faed-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="6faed-104">句法</span><span class="sxs-lookup"><span data-stu-id="6faed-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="6faed-105">說明</span><span class="sxs-lookup"><span data-stu-id="6faed-105">DESCRIPTION</span></span>
<span data-ttu-id="6faed-106">Test-AzStackHCIConnection 驗證來自內部部署叢集節點的連線至 Azure 堆疊 HCI 所需的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="6faed-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="6faed-107">示例</span><span class="sxs-lookup"><span data-stu-id="6faed-107">EXAMPLES</span></span>

### <span data-ttu-id="6faed-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6faed-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
<span data-ttu-id="6faed-109">在其中一個叢集節點上喚醒。</span><span class="sxs-lookup"><span data-stu-id="6faed-109">Invoking on one of the cluster node.</span></span> <span data-ttu-id="6faed-110">成功案例。</span><span class="sxs-lookup"><span data-stu-id="6faed-110">Success case.</span></span>

### <span data-ttu-id="6faed-111">範例2</span><span class="sxs-lookup"><span data-stu-id="6faed-111">EXAMPLE 2</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
<span data-ttu-id="6faed-112">在其中一個叢集節點上喚醒。</span><span class="sxs-lookup"><span data-stu-id="6faed-112">Invoking on one of the cluster node.</span></span> <span data-ttu-id="6faed-113">失敗的情況。</span><span class="sxs-lookup"><span data-stu-id="6faed-113">Failed case.</span></span>

## <span data-ttu-id="6faed-114">參數</span><span class="sxs-lookup"><span data-stu-id="6faed-114">PARAMETERS</span></span>

### <span data-ttu-id="6faed-115">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="6faed-115">-ComputerName</span></span>
<span data-ttu-id="6faed-116">指定登錄至 Azure 之內部部署群集中的其中一個叢集節點。</span><span class="sxs-lookup"><span data-stu-id="6faed-116">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="6faed-117">-認證</span><span class="sxs-lookup"><span data-stu-id="6faed-117">-Credential</span></span>
<span data-ttu-id="6faed-118">指定 ComputerName 的認證。</span><span class="sxs-lookup"><span data-stu-id="6faed-118">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="6faed-119">[預設值] 是執行 Cmdlet 的目前使用者。</span><span class="sxs-lookup"><span data-stu-id="6faed-119">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="6faed-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="6faed-120">-EnvironmentName</span></span>
<span data-ttu-id="6faed-121">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="6faed-121">Specifies the Azure Environment.</span></span>
<span data-ttu-id="6faed-122">預設值為 AzureCloud。</span><span class="sxs-lookup"><span data-stu-id="6faed-122">Default is AzureCloud.</span></span>
<span data-ttu-id="6faed-123">有效值為 AzureCloud、AzureChinaCloud、AzureUSGovernment、AzureGermanCloud、AzurePPE</span><span class="sxs-lookup"><span data-stu-id="6faed-123">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="6faed-124">-Region</span><span class="sxs-lookup"><span data-stu-id="6faed-124">-Region</span></span>
<span data-ttu-id="6faed-125">指定要連接的地區。</span><span class="sxs-lookup"><span data-stu-id="6faed-125">Specifies the Region to connect to.</span></span>
<span data-ttu-id="6faed-126">除非是 [無中的區域]，否則不使用。</span><span class="sxs-lookup"><span data-stu-id="6faed-126">Not used unless it is Canary region.</span></span>

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

### <span data-ttu-id="6faed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6faed-127">CommonParameters</span></span>
<span data-ttu-id="6faed-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6faed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6faed-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6faed-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6faed-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6faed-130">INPUTS</span></span>

## <span data-ttu-id="6faed-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6faed-131">OUTPUTS</span></span>

### <span data-ttu-id="6faed-132">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="6faed-132">PSCustomObject.</span></span> <span data-ttu-id="6faed-133">在 PSCustomObject 中傳回下列屬性</span><span class="sxs-lookup"><span data-stu-id="6faed-133">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="6faed-134">測試：執行的測試名稱。</span><span class="sxs-lookup"><span data-stu-id="6faed-134">Test: Name of the test performed.</span></span>
### <span data-ttu-id="6faed-135">EndpointTested：測試中使用的端點。</span><span class="sxs-lookup"><span data-stu-id="6faed-135">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="6faed-136">IsRequired： True 或 False</span><span class="sxs-lookup"><span data-stu-id="6faed-136">IsRequired: True or False</span></span>
### <span data-ttu-id="6faed-137">結果：成功或失敗</span><span class="sxs-lookup"><span data-stu-id="6faed-137">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="6faed-138">FailedNodes：測試失敗的節點清單。</span><span class="sxs-lookup"><span data-stu-id="6faed-138">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="6faed-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6faed-139">NOTES</span></span>

## <span data-ttu-id="6faed-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="6faed-140">RELATED LINKS</span></span>
