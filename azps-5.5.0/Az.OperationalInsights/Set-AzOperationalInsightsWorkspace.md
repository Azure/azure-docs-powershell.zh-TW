---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142014"
---
# <span data-ttu-id="e8d34-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e8d34-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="e8d34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8d34-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d34-103">更新工作區。</span><span class="sxs-lookup"><span data-stu-id="e8d34-103">Updates a workspace.</span></span>

## <span data-ttu-id="e8d34-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8d34-104">SYNTAX</span></span>

### <span data-ttu-id="e8d34-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="e8d34-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="e8d34-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e8d34-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="e8d34-107">說明</span><span class="sxs-lookup"><span data-stu-id="e8d34-107">DESCRIPTION</span></span>
<span data-ttu-id="e8d34-108">AzOperationalInsightsWorkspace Cmdlet 會變更工作區的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="e8d34-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="e8d34-109">示例</span><span class="sxs-lookup"><span data-stu-id="e8d34-109">EXAMPLES</span></span>

### <span data-ttu-id="e8d34-110">範例1：依名稱修改工作區</span><span class="sxs-lookup"><span data-stu-id="e8d34-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="e8d34-111">這個命令會修改名為 ContosoResourceGroup 之資源群組中名為 MyWorkspace 之工作區的 SKU 及標記。</span><span class="sxs-lookup"><span data-stu-id="e8d34-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="e8d34-112">範例2：使用管線更新工作區</span><span class="sxs-lookup"><span data-stu-id="e8d34-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="e8d34-113">這個命令會使用 Get-AzOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkSpace 的工作區，然後使用管線運算子將 SKU 傳送到 **AzOperationalInsightsWorkspace** Cmdlet，以將 SKU 設定為 Premium。</span><span class="sxs-lookup"><span data-stu-id="e8d34-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="e8d34-114">參數</span><span class="sxs-lookup"><span data-stu-id="e8d34-114">PARAMETERS</span></span>

### <span data-ttu-id="e8d34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d34-115">-DefaultProfile</span></span>
<span data-ttu-id="e8d34-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e8d34-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8d34-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8d34-117">-Name</span></span>
<span data-ttu-id="e8d34-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="e8d34-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d34-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="e8d34-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="e8d34-120">存取工作區接收的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="e8d34-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="e8d34-121">值應為 [Enabled] 或 "Disabled"</span><span class="sxs-lookup"><span data-stu-id="e8d34-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="e8d34-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="e8d34-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="e8d34-123">用於存取工作區查詢的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="e8d34-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="e8d34-124">值應為 [Enabled] 或 "Disabled"</span><span class="sxs-lookup"><span data-stu-id="e8d34-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="e8d34-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8d34-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8d34-126">指定 Azure 資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e8d34-126">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d34-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e8d34-127">-RetentionInDays</span></span>
<span data-ttu-id="e8d34-128">工作區資料保留天數（天）。</span><span class="sxs-lookup"><span data-stu-id="e8d34-128">The workspace data retention in days.</span></span> <span data-ttu-id="e8d34-129">730 days 是所有其他 Sku 允許的上限</span><span class="sxs-lookup"><span data-stu-id="e8d34-129">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d34-130">-Sku</span><span class="sxs-lookup"><span data-stu-id="e8d34-130">-Sku</span></span>
<span data-ttu-id="e8d34-131">指定工作區的服務層級。</span><span class="sxs-lookup"><span data-stu-id="e8d34-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="e8d34-132">有效值為：</span><span class="sxs-lookup"><span data-stu-id="e8d34-132">Valid values are:</span></span> 
- <span data-ttu-id="e8d34-133">空閒</span><span class="sxs-lookup"><span data-stu-id="e8d34-133">free</span></span>
- <span data-ttu-id="e8d34-134">標準</span><span class="sxs-lookup"><span data-stu-id="e8d34-134">standard</span></span>
- <span data-ttu-id="e8d34-135">佳</span><span class="sxs-lookup"><span data-stu-id="e8d34-135">premium</span></span>
- <span data-ttu-id="e8d34-136">pernode</span><span class="sxs-lookup"><span data-stu-id="e8d34-136">pernode</span></span>
- <span data-ttu-id="e8d34-137">獨立</span><span class="sxs-lookup"><span data-stu-id="e8d34-137">standalone</span></span>
- <span data-ttu-id="e8d34-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="e8d34-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d34-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8d34-139">-Tag</span></span>
<span data-ttu-id="e8d34-140">工作區的資源標記。</span><span class="sxs-lookup"><span data-stu-id="e8d34-140">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d34-141">-工作區</span><span class="sxs-lookup"><span data-stu-id="e8d34-141">-Workspace</span></span>
<span data-ttu-id="e8d34-142">指定要更新的工作區。</span><span class="sxs-lookup"><span data-stu-id="e8d34-142">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d34-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d34-143">CommonParameters</span></span>
<span data-ttu-id="e8d34-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8d34-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d34-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8d34-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d34-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e8d34-146">INPUTS</span></span>

### <span data-ttu-id="e8d34-147">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="e8d34-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e8d34-148">System.object</span><span class="sxs-lookup"><span data-stu-id="e8d34-148">System.String</span></span>

### <span data-ttu-id="e8d34-149">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e8d34-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e8d34-150">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e8d34-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e8d34-151">輸出</span><span class="sxs-lookup"><span data-stu-id="e8d34-151">OUTPUTS</span></span>

### <span data-ttu-id="e8d34-152">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="e8d34-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="e8d34-153">筆記</span><span class="sxs-lookup"><span data-stu-id="e8d34-153">NOTES</span></span>

## <span data-ttu-id="e8d34-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8d34-154">RELATED LINKS</span></span>

[<span data-ttu-id="e8d34-155">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e8d34-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="e8d34-156">AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e8d34-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


