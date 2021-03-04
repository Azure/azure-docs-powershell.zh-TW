---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 92a9e1820af2e850af6c3abaca71a7be1f15ed5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901670"
---
# <span data-ttu-id="c1dab-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="c1dab-101">Get-AzResource</span></span>

## <span data-ttu-id="c1dab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1dab-102">SYNOPSIS</span></span>

<span data-ttu-id="c1dab-103">獲得資源。</span><span class="sxs-lookup"><span data-stu-id="c1dab-103">Gets resources.</span></span>

## <span data-ttu-id="c1dab-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1dab-104">SYNTAX</span></span>

### <span data-ttu-id="c1dab-105">ByTagNameValueParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c1dab-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1dab-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1dab-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1dab-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1dab-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1dab-108">描述</span><span class="sxs-lookup"><span data-stu-id="c1dab-108">DESCRIPTION</span></span>

<span data-ttu-id="c1dab-109">**Get-AzResource** Cmdlet 會取得 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="c1dab-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="c1dab-110">例子</span><span class="sxs-lookup"><span data-stu-id="c1dab-110">EXAMPLES</span></span>

### <span data-ttu-id="c1dab-111">範例 1：取得目前訂閱的所有資源</span><span class="sxs-lookup"><span data-stu-id="c1dab-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzResource | ft

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

<span data-ttu-id="c1dab-112">此命令會獲得目前訂閱的所有資源。</span><span class="sxs-lookup"><span data-stu-id="c1dab-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="c1dab-113">範例 2：取得資源群組中所有的資源</span><span class="sxs-lookup"><span data-stu-id="c1dab-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="c1dab-114">此命令會獲得資源群組 "testRG" 的所有資源。</span><span class="sxs-lookup"><span data-stu-id="c1dab-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="c1dab-115">範例 3：取得資源群組符合所提供的萬用字元的所有資源</span><span class="sxs-lookup"><span data-stu-id="c1dab-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="c1dab-116">此命令會以「其他」方式，獲得其所屬資源群組的所有資源。</span><span class="sxs-lookup"><span data-stu-id="c1dab-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="c1dab-117">範例 4：使用指定名稱取得所有資源</span><span class="sxs-lookup"><span data-stu-id="c1dab-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="c1dab-118">此命令會獲得資源名稱為"testMS"的所有資源。</span><span class="sxs-lookup"><span data-stu-id="c1dab-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="c1dab-119">範例 5：取得名稱符合所提供的萬用字元的所有資源</span><span class="sxs-lookup"><span data-stu-id="c1dab-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="c1dab-120">此命令會獲得資源名稱以「測試」開頭的所有資源。</span><span class="sxs-lookup"><span data-stu-id="c1dab-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="c1dab-121">範例 6：取得給定資源類型的所有資源</span><span class="sxs-lookup"><span data-stu-id="c1dab-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="c1dab-122">此命令會獲得目前訂閱中虛擬機器的所有資源。</span><span class="sxs-lookup"><span data-stu-id="c1dab-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="c1dab-123">範例 7：根據資源識別碼取得資源</span><span class="sxs-lookup"><span data-stu-id="c1dab-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="c1dab-124">此命令會使用提供的資源識別碼來獲得資源，這是資源群組 "testRG" 中稱為 "testMS" 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c1dab-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="c1dab-125">參數</span><span class="sxs-lookup"><span data-stu-id="c1dab-125">PARAMETERS</span></span>

### <span data-ttu-id="c1dab-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c1dab-126">-ApiVersion</span></span>

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

### <span data-ttu-id="c1dab-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1dab-127">-DefaultProfile</span></span>
<span data-ttu-id="c1dab-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c1dab-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1dab-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="c1dab-129">-ExpandProperties</span></span>
<span data-ttu-id="c1dab-130">指定時，展開資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="c1dab-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="c1dab-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1dab-131">-Name</span></span>
<span data-ttu-id="c1dab-132">要 (的資源) 名稱。</span><span class="sxs-lookup"><span data-stu-id="c1dab-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="c1dab-133">此參數支援字串開頭和/或結尾的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c1dab-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="c1dab-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c1dab-134">-ODataQuery</span></span>

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

### <span data-ttu-id="c1dab-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="c1dab-135">-Pre</span></span>

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

### <span data-ttu-id="c1dab-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1dab-136">-ResourceGroupName</span></span>
<span data-ttu-id="c1dab-137">已取回 (資源) 所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c1dab-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="c1dab-138">此參數支援字串開頭和/或結尾的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c1dab-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="c1dab-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1dab-139">-ResourceId</span></span>
<span data-ttu-id="c1dab-140">指定完整資源識別碼，如下列範例所示 `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="c1dab-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

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

### <span data-ttu-id="c1dab-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c1dab-141">-ResourceType</span></span>
<span data-ttu-id="c1dab-142">要取回的資源 () 類型。</span><span class="sxs-lookup"><span data-stu-id="c1dab-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="c1dab-143">例如，Microsoft.Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="c1dab-143">For example, Microsoft.Compute/virtualMachines</span></span>

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

### <span data-ttu-id="c1dab-144">-標記</span><span class="sxs-lookup"><span data-stu-id="c1dab-144">-Tag</span></span>

<span data-ttu-id="c1dab-145">獲得具有指定 Azure 標記的資源。</span><span class="sxs-lookup"><span data-stu-id="c1dab-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="c1dab-146">輸入包含名稱鍵或名稱與值索引鍵的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c1dab-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="c1dab-147">不支援萬用字元。「標記」是一組名稱值，您可以將它用於資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="c1dab-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="c1dab-148">使用標記來分類資源，例如按照部門或成本中心，或追蹤資源的附注或批註。</span><span class="sxs-lookup"><span data-stu-id="c1dab-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="c1dab-149">若要新增標籤至資源，請使用標籤或 Cmdlet New-AzResource標記Set-AzResource參數。</span><span class="sxs-lookup"><span data-stu-id="c1dab-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="c1dab-150">若要建立預先定義的標籤，請使用 New-AzTag Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1dab-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="c1dab-151">有關 Windows PowerShell 中雜湊表格的協助，請執行 'Get-help about_Hashtables'。</span><span class="sxs-lookup"><span data-stu-id="c1dab-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

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

### <span data-ttu-id="c1dab-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="c1dab-152">-TagName</span></span>
<span data-ttu-id="c1dab-153">要取回的資源 (標記) 鍵。</span><span class="sxs-lookup"><span data-stu-id="c1dab-153">The key in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="c1dab-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="c1dab-154">-TagValue</span></span>
<span data-ttu-id="c1dab-155">要取回的資源 (標記) 的值。</span><span class="sxs-lookup"><span data-stu-id="c1dab-155">The value in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="c1dab-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1dab-156">CommonParameters</span></span>
<span data-ttu-id="c1dab-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1dab-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1dab-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1dab-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1dab-159">輸入</span><span class="sxs-lookup"><span data-stu-id="c1dab-159">INPUTS</span></span>

### <span data-ttu-id="c1dab-160">System.String</span><span class="sxs-lookup"><span data-stu-id="c1dab-160">System.String</span></span>

## <span data-ttu-id="c1dab-161">輸出</span><span class="sxs-lookup"><span data-stu-id="c1dab-161">OUTPUTS</span></span>

### <span data-ttu-id="c1dab-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="c1dab-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="c1dab-163">筆記</span><span class="sxs-lookup"><span data-stu-id="c1dab-163">NOTES</span></span>

## <span data-ttu-id="c1dab-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1dab-164">RELATED LINKS</span></span>

[<span data-ttu-id="c1dab-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="c1dab-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="c1dab-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="c1dab-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="c1dab-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="c1dab-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="c1dab-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="c1dab-168">Set-AzResource</span></span>](./Set-AzResource.md)