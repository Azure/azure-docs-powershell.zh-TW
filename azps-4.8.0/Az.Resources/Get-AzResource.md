---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: e1748bb3dbb5c2bb86f02ef9ec58d0d1eec55ba9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127889"
---
# <span data-ttu-id="d24c4-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="d24c4-101">Get-AzResource</span></span>

## <span data-ttu-id="d24c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d24c4-102">SYNOPSIS</span></span>

<span data-ttu-id="d24c4-103">取得資源。</span><span class="sxs-lookup"><span data-stu-id="d24c4-103">Gets resources.</span></span>

## <span data-ttu-id="d24c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="d24c4-104">SYNTAX</span></span>

### <span data-ttu-id="d24c4-105">ByTagNameValueParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d24c4-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d24c4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d24c4-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d24c4-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d24c4-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d24c4-108">說明</span><span class="sxs-lookup"><span data-stu-id="d24c4-108">DESCRIPTION</span></span>

<span data-ttu-id="d24c4-109">**AzResource** Cmdlet 會取得 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="d24c4-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="d24c4-110">示例</span><span class="sxs-lookup"><span data-stu-id="d24c4-110">EXAMPLES</span></span>

### <span data-ttu-id="d24c4-111">範例1：取得目前訂閱中的所有資源</span><span class="sxs-lookup"><span data-stu-id="d24c4-111">Example 1: Get all resources in the current subscription</span></span>

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

<span data-ttu-id="d24c4-112">這個命令會取得目前訂閱中的所有資源。</span><span class="sxs-lookup"><span data-stu-id="d24c4-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="d24c4-113">範例2：取得資源群組中的所有資源</span><span class="sxs-lookup"><span data-stu-id="d24c4-113">Example 2: Get all resources in a resource group</span></span>

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

<span data-ttu-id="d24c4-114">這個命令會取得資源群組 "testRG" 中的所有資源。</span><span class="sxs-lookup"><span data-stu-id="d24c4-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="d24c4-115">範例3：取得資源群組與提供的萬用字元相符的所有資源</span><span class="sxs-lookup"><span data-stu-id="d24c4-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="d24c4-116">這個命令會取得其資源群組與「其他」有關的所有資源。</span><span class="sxs-lookup"><span data-stu-id="d24c4-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="d24c4-117">範例4：取得具有指定名稱的所有資源</span><span class="sxs-lookup"><span data-stu-id="d24c4-117">Example 4: Get all resources with a given name</span></span>

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

<span data-ttu-id="d24c4-118">這個命令會取得資源名稱為 "testVM" 的所有資源。</span><span class="sxs-lookup"><span data-stu-id="d24c4-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="d24c4-119">範例5：取得名稱與提供的萬用字元相符的所有資源</span><span class="sxs-lookup"><span data-stu-id="d24c4-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="d24c4-120">這個命令會取得其資源名稱以「test」開頭的所有資源。</span><span class="sxs-lookup"><span data-stu-id="d24c4-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="d24c4-121">範例6：取得指定資源類型的所有資源</span><span class="sxs-lookup"><span data-stu-id="d24c4-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="d24c4-122">這個命令會在目前的訂閱中取得虛擬機器的所有資源。</span><span class="sxs-lookup"><span data-stu-id="d24c4-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="d24c4-123">範例7：依資源識別碼取得資源</span><span class="sxs-lookup"><span data-stu-id="d24c4-123">Example 7: Get a resource by resource id</span></span>

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

<span data-ttu-id="d24c4-124">這個命令會取得具有提供之資源識別碼的資源，這是資源群組 "testRG" 中稱為 "testVM" 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d24c4-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="d24c4-125">參數</span><span class="sxs-lookup"><span data-stu-id="d24c4-125">PARAMETERS</span></span>

### <span data-ttu-id="d24c4-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d24c4-126">-ApiVersion</span></span>

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

### <span data-ttu-id="d24c4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24c4-127">-DefaultProfile</span></span>
<span data-ttu-id="d24c4-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d24c4-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d24c4-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="d24c4-129">-ExpandProperties</span></span>
<span data-ttu-id="d24c4-130">指定時，會展開資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="d24c4-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="d24c4-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="d24c4-131">-Name</span></span>
<span data-ttu-id="d24c4-132">要檢索) 資源 (s 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d24c4-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="d24c4-133">這個參數支援字串開頭和/或結尾的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="d24c4-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="d24c4-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d24c4-134">-ODataQuery</span></span>

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

### <span data-ttu-id="d24c4-135">-預先</span><span class="sxs-lookup"><span data-stu-id="d24c4-135">-Pre</span></span>

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

### <span data-ttu-id="d24c4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24c4-136">-ResourceGroupName</span></span>
<span data-ttu-id="d24c4-137">[資源] 群組) 所檢索的資源 (s。</span><span class="sxs-lookup"><span data-stu-id="d24c4-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="d24c4-138">這個參數支援字串開頭和/或結尾的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="d24c4-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="d24c4-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d24c4-139">-ResourceId</span></span>
<span data-ttu-id="d24c4-140">指定完全合格的資源識別碼，如下列範例所示 `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="d24c4-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

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

### <span data-ttu-id="d24c4-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d24c4-141">-ResourceType</span></span>
<span data-ttu-id="d24c4-142">要檢索) 資源的資源類型 (s。</span><span class="sxs-lookup"><span data-stu-id="d24c4-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="d24c4-143">例如，Microsoft. 計算/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="d24c4-143">For example, Microsoft.Compute/virtualMachines</span></span>

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

### <span data-ttu-id="d24c4-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="d24c4-144">-Tag</span></span>

<span data-ttu-id="d24c4-145">取得具有指定 Azure 標記的資源。</span><span class="sxs-lookup"><span data-stu-id="d24c4-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="d24c4-146">輸入具有 [鍵] 或 [名稱] 和 [值] 鍵的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d24c4-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="d24c4-147">不支援萬用字元。[標記] 是您可以套用至資源和資源群組的名稱-值對。</span><span class="sxs-lookup"><span data-stu-id="d24c4-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="d24c4-148">使用標籤將資源分類（例如 [部門] 或 [成本中心]），或追蹤資源的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="d24c4-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="d24c4-149">若要新增標籤至資源，請使用 New-AzResource 或 Set-AzResource Cmdlet 的 Tag 參數。</span><span class="sxs-lookup"><span data-stu-id="d24c4-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="d24c4-150">若要建立預先定義的標記，請使用 New-AzTag Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d24c4-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="d24c4-151">如需有關 Windows PowerShell 中的雜湊資料表的說明，請執行「Get-help about_Hashtables」。</span><span class="sxs-lookup"><span data-stu-id="d24c4-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

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

### <span data-ttu-id="d24c4-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="d24c4-152">-TagName</span></span>
<span data-ttu-id="d24c4-153">要檢索) 資源的標籤中的索引鍵 (s。</span><span class="sxs-lookup"><span data-stu-id="d24c4-153">The key in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="d24c4-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="d24c4-154">-TagValue</span></span>
<span data-ttu-id="d24c4-155">要檢索之資源 (s 的標籤中的值) 。</span><span class="sxs-lookup"><span data-stu-id="d24c4-155">The value in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="d24c4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24c4-156">CommonParameters</span></span>
<span data-ttu-id="d24c4-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d24c4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24c4-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d24c4-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24c4-159">輸入</span><span class="sxs-lookup"><span data-stu-id="d24c4-159">INPUTS</span></span>

### <span data-ttu-id="d24c4-160">System.object</span><span class="sxs-lookup"><span data-stu-id="d24c4-160">System.String</span></span>

## <span data-ttu-id="d24c4-161">輸出</span><span class="sxs-lookup"><span data-stu-id="d24c4-161">OUTPUTS</span></span>

### <span data-ttu-id="d24c4-162">PSResource 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="d24c4-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="d24c4-163">筆記</span><span class="sxs-lookup"><span data-stu-id="d24c4-163">NOTES</span></span>

## <span data-ttu-id="d24c4-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="d24c4-164">RELATED LINKS</span></span>

[<span data-ttu-id="d24c4-165">尋找-AzResource</span><span class="sxs-lookup"><span data-stu-id="d24c4-165">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="d24c4-166">移動流覽 AzResource</span><span class="sxs-lookup"><span data-stu-id="d24c4-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="d24c4-167">新-AzResource</span><span class="sxs-lookup"><span data-stu-id="d24c4-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="d24c4-168">移除-AzResource</span><span class="sxs-lookup"><span data-stu-id="d24c4-168">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="d24c4-169">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="d24c4-169">Set-AzResource</span></span>](./Set-AzResource.md)
