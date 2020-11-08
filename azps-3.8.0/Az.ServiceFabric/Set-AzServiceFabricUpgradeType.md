---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: c29a1bf4b5b60034a8f38ff8388f36997dbddfc7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965739"
---
# <span data-ttu-id="49ed7-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="49ed7-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="49ed7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="49ed7-103">變更群集的 Service Fabric 升級類型。</span><span class="sxs-lookup"><span data-stu-id="49ed7-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="49ed7-104">句法</span><span class="sxs-lookup"><span data-stu-id="49ed7-104">SYNTAX</span></span>

### <span data-ttu-id="49ed7-105">自動</span><span class="sxs-lookup"><span data-stu-id="49ed7-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ed7-106">手動</span><span class="sxs-lookup"><span data-stu-id="49ed7-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ed7-107">說明</span><span class="sxs-lookup"><span data-stu-id="49ed7-107">DESCRIPTION</span></span>
<span data-ttu-id="49ed7-108">使用 [ **設定] AzServiceFabricUpgradeType** ，將 [升級類型] 設定為 [自動] 或 [手動] 與特定的服務結構代碼版本。</span><span class="sxs-lookup"><span data-stu-id="49ed7-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="49ed7-109">示例</span><span class="sxs-lookup"><span data-stu-id="49ed7-109">EXAMPLES</span></span>

### <span data-ttu-id="49ed7-110">範例1</span><span class="sxs-lookup"><span data-stu-id="49ed7-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="49ed7-111">這個命令會將 [群集升級模式] 設定為 [自動]。</span><span class="sxs-lookup"><span data-stu-id="49ed7-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="49ed7-112">參數</span><span class="sxs-lookup"><span data-stu-id="49ed7-112">PARAMETERS</span></span>

### <span data-ttu-id="49ed7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ed7-113">-DefaultProfile</span></span>
<span data-ttu-id="49ed7-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49ed7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49ed7-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="49ed7-115">-Name</span></span>
<span data-ttu-id="49ed7-116">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="49ed7-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ed7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49ed7-117">-ResourceGroupName</span></span>
<span data-ttu-id="49ed7-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49ed7-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ed7-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="49ed7-119">-UpgradeMode</span></span>
<span data-ttu-id="49ed7-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="49ed7-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ed7-121">-版本</span><span class="sxs-lookup"><span data-stu-id="49ed7-121">-Version</span></span>
<span data-ttu-id="49ed7-122">群集代碼版本</span><span class="sxs-lookup"><span data-stu-id="49ed7-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ed7-123">-確認</span><span class="sxs-lookup"><span data-stu-id="49ed7-123">-Confirm</span></span>
<span data-ttu-id="49ed7-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="49ed7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ed7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ed7-125">-WhatIf</span></span>
<span data-ttu-id="49ed7-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49ed7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49ed7-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49ed7-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ed7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ed7-128">CommonParameters</span></span>
<span data-ttu-id="49ed7-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49ed7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ed7-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49ed7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ed7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="49ed7-131">INPUTS</span></span>

### <span data-ttu-id="49ed7-132">System.object</span><span class="sxs-lookup"><span data-stu-id="49ed7-132">System.String</span></span>

### <span data-ttu-id="49ed7-133">ClusterUpgradeMode 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="49ed7-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="49ed7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="49ed7-134">OUTPUTS</span></span>

### <span data-ttu-id="49ed7-135">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="49ed7-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="49ed7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="49ed7-136">NOTES</span></span>

## <span data-ttu-id="49ed7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="49ed7-137">RELATED LINKS</span></span>