---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 4de1e1467e1bc422666b7144f5d5fcd6c30c0c63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907974"
---
# <span data-ttu-id="e4ff2-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="e4ff2-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="e4ff2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e4ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ff2-103">Test-AzStackHCIConnection驗證從內部部署組群節點到 Azure Stack HCI 所需 Azure 服務的連接。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="e4ff2-104">語法</span><span class="sxs-lookup"><span data-stu-id="e4ff2-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="e4ff2-105">描述</span><span class="sxs-lookup"><span data-stu-id="e4ff2-105">DESCRIPTION</span></span>
<span data-ttu-id="e4ff2-106">Test-AzStackHCIConnection驗證從內部部署組群節點到 Azure Stack HCI 所需 Azure 服務的連接。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="e4ff2-107">例子</span><span class="sxs-lookup"><span data-stu-id="e4ff2-107">EXAMPLES</span></span>

### <span data-ttu-id="e4ff2-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e4ff2-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
<span data-ttu-id="e4ff2-109">其中一個組節點上啟動。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-109">Invoking on one of the cluster node.</span></span> <span data-ttu-id="e4ff2-110">成功案例。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-110">Success case.</span></span>

### <span data-ttu-id="e4ff2-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="e4ff2-111">EXAMPLE 2</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
<span data-ttu-id="e4ff2-112">其中一個組節點上啟動。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-112">Invoking on one of the cluster node.</span></span> <span data-ttu-id="e4ff2-113">失敗案例。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-113">Failed case.</span></span>

## <span data-ttu-id="e4ff2-114">參數</span><span class="sxs-lookup"><span data-stu-id="e4ff2-114">PARAMETERS</span></span>

### <span data-ttu-id="e4ff2-115">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="e4ff2-115">-ComputerName</span></span>
<span data-ttu-id="e4ff2-116">指定要註冊至 Azure 之內部部署組集中的其中一個集區節點。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-116">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="e4ff2-117">-認證</span><span class="sxs-lookup"><span data-stu-id="e4ff2-117">-Credential</span></span>
<span data-ttu-id="e4ff2-118">指定 ComputerName 的認證。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-118">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="e4ff2-119">預設值為執行 Cmdlet 的目前使用者。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-119">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="e4ff2-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e4ff2-120">-EnvironmentName</span></span>
<span data-ttu-id="e4ff2-121">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-121">Specifies the Azure Environment.</span></span>
<span data-ttu-id="e4ff2-122">預設值為 AzureCloud。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-122">Default is AzureCloud.</span></span>
<span data-ttu-id="e4ff2-123">有效的值為 AzureCloud、AzureChinaCloud、AzureUSGovernment、AzureGermanCloud、AzurePPE</span><span class="sxs-lookup"><span data-stu-id="e4ff2-123">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="e4ff2-124">-區域</span><span class="sxs-lookup"><span data-stu-id="e4ff2-124">-Region</span></span>
<span data-ttu-id="e4ff2-125">指定要連接的區域。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-125">Specifies the Region to connect to.</span></span>
<span data-ttu-id="e4ff2-126">除非是 Canary 地區，否則不會使用。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-126">Not used unless it is Canary region.</span></span>

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

### <span data-ttu-id="e4ff2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ff2-127">CommonParameters</span></span>
<span data-ttu-id="e4ff2-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ff2-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4ff2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ff2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e4ff2-130">INPUTS</span></span>

## <span data-ttu-id="e4ff2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e4ff2-131">OUTPUTS</span></span>

### <span data-ttu-id="e4ff2-132">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="e4ff2-132">PSCustomObject.</span></span> <span data-ttu-id="e4ff2-133">在 PSCustomObject 中返回下列屬性</span><span class="sxs-lookup"><span data-stu-id="e4ff2-133">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="e4ff2-134">測試：執行的測試名稱。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-134">Test: Name of the test performed.</span></span>
### <span data-ttu-id="e4ff2-135">端點測試：用於測試的端點。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-135">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="e4ff2-136">IsRequired：True 或 False</span><span class="sxs-lookup"><span data-stu-id="e4ff2-136">IsRequired: True or False</span></span>
### <span data-ttu-id="e4ff2-137">結果：成功或失敗</span><span class="sxs-lookup"><span data-stu-id="e4ff2-137">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="e4ff2-138">失敗：測試失敗之節點的清單。</span><span class="sxs-lookup"><span data-stu-id="e4ff2-138">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="e4ff2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e4ff2-139">NOTES</span></span>

## <span data-ttu-id="e4ff2-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4ff2-140">RELATED LINKS</span></span>
