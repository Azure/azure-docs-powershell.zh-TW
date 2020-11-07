---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
ms.openlocfilehash: aa9a0c3a1e06c7ef4a66c58f3039bda19d4824ee
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801149"
---
# <span data-ttu-id="2e575-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2e575-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="2e575-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e575-102">SYNOPSIS</span></span>

<span data-ttu-id="2e575-103">取得資源。</span><span class="sxs-lookup"><span data-stu-id="2e575-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e575-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e575-104">SYNTAX</span></span>

### <span data-ttu-id="2e575-105">ByTagNameValueParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2e575-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzureRmResource [[-Name] <String>] [-ResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-TagName <String>] [-TagValue <String>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e575-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e575-106">ByResourceId</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e575-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e575-107">ByTagObjectParameterSet</span></span>
```
Get-AzureRmResource [[-Name] <String>] [-ResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e575-108">說明</span><span class="sxs-lookup"><span data-stu-id="2e575-108">DESCRIPTION</span></span>

<span data-ttu-id="2e575-109">**AzureRmResource** Cmdlet 會取得 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="2e575-109">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="2e575-110">示例</span><span class="sxs-lookup"><span data-stu-id="2e575-110">EXAMPLES</span></span>

### <span data-ttu-id="2e575-111">範例1：取得目前訂閱中的所有資源</span><span class="sxs-lookup"><span data-stu-id="2e575-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzureRmResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

<span data-ttu-id="2e575-112">這個命令會取得目前訂閱中的所有資源。</span><span class="sxs-lookup"><span data-stu-id="2e575-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="2e575-113">範例2：取得資源群組中的所有資源</span><span class="sxs-lookup"><span data-stu-id="2e575-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzureRmResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="2e575-114">這個命令會取得資源群組 "testRG" 中的所有資源。</span><span class="sxs-lookup"><span data-stu-id="2e575-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="2e575-115">範例3：取得資源群組與提供的萬用字元相符的所有資源</span><span class="sxs-lookup"><span data-stu-id="2e575-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzureRmResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="2e575-116">這個命令會取得其資源群組與「其他」有關的所有資源。</span><span class="sxs-lookup"><span data-stu-id="2e575-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="2e575-117">範例4：取得具有指定名稱的所有資源</span><span class="sxs-lookup"><span data-stu-id="2e575-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzureRmResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="2e575-118">這個命令會取得資源名稱為 "testVM" 的所有資源。</span><span class="sxs-lookup"><span data-stu-id="2e575-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="2e575-119">範例5：取得名稱與提供的萬用字元相符的所有資源</span><span class="sxs-lookup"><span data-stu-id="2e575-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzureRmResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="2e575-120">這個命令會取得其資源名稱以「test」開頭的所有資源。</span><span class="sxs-lookup"><span data-stu-id="2e575-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="2e575-121">範例6：取得指定資源類型的所有資源</span><span class="sxs-lookup"><span data-stu-id="2e575-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="2e575-122">這個命令會在目前的訂閱中取得虛擬機器的所有資源。</span><span class="sxs-lookup"><span data-stu-id="2e575-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="2e575-123">範例7：依資源識別碼取得資源</span><span class="sxs-lookup"><span data-stu-id="2e575-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzureRmResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="2e575-124">這個命令會取得具有提供之資源識別碼的資源，這是資源群組 "testRG" 中稱為 "testVM" 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2e575-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="2e575-125">參數</span><span class="sxs-lookup"><span data-stu-id="2e575-125">PARAMETERS</span></span>

### <span data-ttu-id="2e575-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2e575-126">-ApiVersion</span></span>

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

### <span data-ttu-id="2e575-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e575-127">-DefaultProfile</span></span>
<span data-ttu-id="2e575-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2e575-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e575-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="2e575-129">-ExpandProperties</span></span>
<span data-ttu-id="2e575-130">指定時，會展開資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="2e575-130">When specified, expands the properties of the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e575-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e575-131">-Name</span></span>
<span data-ttu-id="2e575-132">要檢索) 資源 (s 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e575-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="2e575-133">這個參數支援字串開頭和/或結尾的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="2e575-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e575-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="2e575-134">-ODataQuery</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e575-135">-預先</span><span class="sxs-lookup"><span data-stu-id="2e575-135">-Pre</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e575-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e575-136">-ResourceGroupName</span></span>
<span data-ttu-id="2e575-137">[資源] 群組 retireved 所屬的資源 (s) 。</span><span class="sxs-lookup"><span data-stu-id="2e575-137">The resource group the resource(s) that is retireved belongs in.</span></span> <span data-ttu-id="2e575-138">這個參數支援字串開頭和/或結尾的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="2e575-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e575-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e575-139">-ResourceId</span></span>
<span data-ttu-id="2e575-140">指定完全合格的資源識別碼，如下列範例所示 `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="2e575-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e575-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2e575-141">-ResourceType</span></span>
<span data-ttu-id="2e575-142">要檢索) 資源的資源類型 (s。</span><span class="sxs-lookup"><span data-stu-id="2e575-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="2e575-143">例如，Microsoft. 計算/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="2e575-143">For example, Microsoft.Compute/virtualMachines</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e575-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e575-144">-Tag</span></span>

<span data-ttu-id="2e575-145">取得具有指定 Azure 標記的資源。</span><span class="sxs-lookup"><span data-stu-id="2e575-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="2e575-146">輸入具有 [鍵] 或 [名稱] 和 [值] 鍵的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2e575-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="2e575-147">不支援萬用字元。[標記] 是您可以套用至資源和資源群組的名稱-值對。</span><span class="sxs-lookup"><span data-stu-id="2e575-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="2e575-148">使用標籤將資源分類（例如 [部門] 或 [成本中心]），或追蹤資源的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="2e575-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="2e575-149">若要新增標籤至資源，請使用 New-AzureRmResource 或 Set-AzureRmResource Cmdlet 的 Tag 參數。</span><span class="sxs-lookup"><span data-stu-id="2e575-149">To add a tag to a resource, use the Tag parameter of the New-AzureRmResource or Set-AzureRmResource cmdlets.</span></span> <span data-ttu-id="2e575-150">若要建立預先定義的標記，請使用 New-AzureRmTag Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e575-150">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span> <span data-ttu-id="2e575-151">如需有關 Windows PowerShell 中的雜湊資料表的說明，請執行「Get-help about_Hashtables」。</span><span class="sxs-lookup"><span data-stu-id="2e575-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e575-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="2e575-152">-TagName</span></span>
<span data-ttu-id="2e575-153">要檢索) 資源的標籤中的索引鍵 (s。</span><span class="sxs-lookup"><span data-stu-id="2e575-153">The key in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e575-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="2e575-154">-TagValue</span></span>
<span data-ttu-id="2e575-155">要檢索之資源 (s 的標籤中的值) 。</span><span class="sxs-lookup"><span data-stu-id="2e575-155">The value in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e575-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e575-156">CommonParameters</span></span>
<span data-ttu-id="2e575-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e575-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e575-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e575-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e575-159">輸入</span><span class="sxs-lookup"><span data-stu-id="2e575-159">INPUTS</span></span>

### <span data-ttu-id="2e575-160">所有</span><span class="sxs-lookup"><span data-stu-id="2e575-160">None</span></span>

## <span data-ttu-id="2e575-161">輸出</span><span class="sxs-lookup"><span data-stu-id="2e575-161">OUTPUTS</span></span>

### <span data-ttu-id="2e575-162">PSResource 中的 ResourceManagement。</span><span class="sxs-lookup"><span data-stu-id="2e575-162">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="2e575-163">筆記</span><span class="sxs-lookup"><span data-stu-id="2e575-163">NOTES</span></span>

## <span data-ttu-id="2e575-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e575-164">RELATED LINKS</span></span>



[<span data-ttu-id="2e575-165">移動流覽 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2e575-165">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="2e575-166">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2e575-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="2e575-167">移除-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2e575-167">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="2e575-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2e575-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
