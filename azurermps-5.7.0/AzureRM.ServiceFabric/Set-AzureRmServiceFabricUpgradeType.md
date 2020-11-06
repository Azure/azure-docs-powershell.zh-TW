---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 8a675355806a8b4579abcea965a5e0e0b8128207
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454067"
---
# <span data-ttu-id="607de-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="607de-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="607de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="607de-102">SYNOPSIS</span></span>
<span data-ttu-id="607de-103">變更群集的 Service Fabric 升級類型。</span><span class="sxs-lookup"><span data-stu-id="607de-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="607de-104">句法</span><span class="sxs-lookup"><span data-stu-id="607de-104">SYNTAX</span></span>

### <span data-ttu-id="607de-105">自動</span><span class="sxs-lookup"><span data-stu-id="607de-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="607de-106">手動</span><span class="sxs-lookup"><span data-stu-id="607de-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="607de-107">說明</span><span class="sxs-lookup"><span data-stu-id="607de-107">DESCRIPTION</span></span>
<span data-ttu-id="607de-108">使用 [ **設定] AzureRmServiceFabricUpgradeType** ，將 [升級類型] 設定為 [自動] 或 [手動] 與特定的服務結構代碼版本。</span><span class="sxs-lookup"><span data-stu-id="607de-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="607de-109">示例</span><span class="sxs-lookup"><span data-stu-id="607de-109">EXAMPLES</span></span>

### <span data-ttu-id="607de-110">範例1</span><span class="sxs-lookup"><span data-stu-id="607de-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="607de-111">這個命令會將 [群集升級模式] 設定為 [自動]。</span><span class="sxs-lookup"><span data-stu-id="607de-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="607de-112">參數</span><span class="sxs-lookup"><span data-stu-id="607de-112">PARAMETERS</span></span>

### <span data-ttu-id="607de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="607de-113">-DefaultProfile</span></span>
<span data-ttu-id="607de-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="607de-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="607de-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="607de-115">-Name</span></span>
<span data-ttu-id="607de-116">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="607de-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607de-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="607de-117">-ResourceGroupName</span></span>
<span data-ttu-id="607de-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="607de-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607de-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="607de-119">-UpgradeMode</span></span>
<span data-ttu-id="607de-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="607de-120">ClusterUpgradeMode</span></span>

```yaml
Type: ClusterUpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="607de-121">-版本</span><span class="sxs-lookup"><span data-stu-id="607de-121">-Version</span></span>
<span data-ttu-id="607de-122">群集程式碼版本。</span><span class="sxs-lookup"><span data-stu-id="607de-122">Cluster code version.</span></span>

```yaml
Type: String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="607de-123">-確認</span><span class="sxs-lookup"><span data-stu-id="607de-123">-Confirm</span></span>
<span data-ttu-id="607de-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="607de-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607de-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="607de-125">-WhatIf</span></span>
<span data-ttu-id="607de-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="607de-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="607de-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="607de-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607de-128">CommonParameters</span></span>
<span data-ttu-id="607de-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="607de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607de-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="607de-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607de-131">輸入</span><span class="sxs-lookup"><span data-stu-id="607de-131">INPUTS</span></span>

### <span data-ttu-id="607de-132">ClusterUpgradeMode 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="607de-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="607de-133">System.object</span><span class="sxs-lookup"><span data-stu-id="607de-133">System.String</span></span>

## <span data-ttu-id="607de-134">輸出</span><span class="sxs-lookup"><span data-stu-id="607de-134">OUTPUTS</span></span>

### <span data-ttu-id="607de-135">PsCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="607de-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="607de-136">筆記</span><span class="sxs-lookup"><span data-stu-id="607de-136">NOTES</span></span>

## <span data-ttu-id="607de-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="607de-137">RELATED LINKS</span></span>

