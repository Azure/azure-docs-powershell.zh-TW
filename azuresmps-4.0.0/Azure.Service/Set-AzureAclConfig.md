---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967878"
---
# <span data-ttu-id="58086-101">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="58086-101">Set-AzureAclConfig</span></span>

## <span data-ttu-id="58086-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58086-102">SYNOPSIS</span></span>
<span data-ttu-id="58086-103">修改 ACL 設定物件。</span><span class="sxs-lookup"><span data-stu-id="58086-103">Modifies an ACL configuration object.</span></span>

## <span data-ttu-id="58086-104">句法</span><span class="sxs-lookup"><span data-stu-id="58086-104">SYNTAX</span></span>

### <span data-ttu-id="58086-105">AddRule</span><span class="sxs-lookup"><span data-stu-id="58086-105">AddRule</span></span>
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="58086-106">RemoveRule</span><span class="sxs-lookup"><span data-stu-id="58086-106">RemoveRule</span></span>
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="58086-107">SetRule</span><span class="sxs-lookup"><span data-stu-id="58086-107">SetRule</span></span>
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="58086-108">說明</span><span class="sxs-lookup"><span data-stu-id="58086-108">DESCRIPTION</span></span>
<span data-ttu-id="58086-109">**AzureAclConfig** Cmdlet 會從現有的 Azure 虛擬機器設定修改存取控制清單 (ACL) 設定物件。</span><span class="sxs-lookup"><span data-stu-id="58086-109">The **Set-AzureAclConfig** cmdlet modifies an access control list (ACL) configuration object from an existing Azure virtual machine configuration.</span></span>

## <span data-ttu-id="58086-110">示例</span><span class="sxs-lookup"><span data-stu-id="58086-110">EXAMPLES</span></span>

### <span data-ttu-id="58086-111">範例1：將規則新增至新的 ACL 配置</span><span class="sxs-lookup"><span data-stu-id="58086-111">Example 1: Add a rule to a new ACL configuration</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

<span data-ttu-id="58086-112">第一個命令會建立 ACL 設定，然後將它儲存在 $Acl 變數中。</span><span class="sxs-lookup"><span data-stu-id="58086-112">The first command creates an ACL configuration, and then stores it in the $Acl variable.</span></span>

<span data-ttu-id="58086-113">第二個命令會將新規則新增至儲存在 $Acl 中的設定。</span><span class="sxs-lookup"><span data-stu-id="58086-113">The second command adds a new rule to the configuration stored in $Acl.</span></span>
<span data-ttu-id="58086-114">此命令會指定規則的動作、子網、順序及描述。</span><span class="sxs-lookup"><span data-stu-id="58086-114">The command specifies an action, subnet, order, and description for the rule.</span></span>

### <span data-ttu-id="58086-115">範例2：在 ACL 設定中修改規則</span><span class="sxs-lookup"><span data-stu-id="58086-115">Example 2: Modify a rule in an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="58086-116">第一個命令會透過使用 **xxxxx Cmdlet，** 在名為 ContosoService 的服務中，取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="58086-116">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="58086-117">命令會使用管線運算子，將該物件傳遞到 **AzureAclConfig** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58086-117">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="58086-118">該 Cmdlet 會取得名為 [Web] 的端點的 ACL 設定。</span><span class="sxs-lookup"><span data-stu-id="58086-118">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="58086-119">該命令會將該 ACL 設定物件儲存在 $Acl 變數中。</span><span class="sxs-lookup"><span data-stu-id="58086-119">The command stores that ACL configuration object in the $Acl variable.</span></span>

<span data-ttu-id="58086-120">第二個命令會修改 ID 為0的規則。</span><span class="sxs-lookup"><span data-stu-id="58086-120">The second command modifies the rule that has the ID of 0.</span></span>
<span data-ttu-id="58086-121">該命令會變更規則的順序及描述。</span><span class="sxs-lookup"><span data-stu-id="58086-121">The command changes the order and the description of the rule.</span></span>

<span data-ttu-id="58086-122">最終命令會使用 **AzureEndpoint** Cmdlet 來設定該虛擬機器的 ACL 設定物件。</span><span class="sxs-lookup"><span data-stu-id="58086-122">The final command sets the ACL configuration object for that virtual machine by using the **Set-AzureEndpoint** cmdlet.</span></span>
<span data-ttu-id="58086-123">此命令也會更新該虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="58086-123">The command also updates that virtual machine.</span></span>

### <span data-ttu-id="58086-124">範例3：從 ACL 設定中移除規則</span><span class="sxs-lookup"><span data-stu-id="58086-124">Example 3: Remove a rule from an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="58086-125">第一個命令會將 ACL 設定物件儲存在 $Acl 變數中。</span><span class="sxs-lookup"><span data-stu-id="58086-125">The first command stores an ACL configuration object in the $Acl variable.</span></span>
<span data-ttu-id="58086-126">這與上一個範例相同。</span><span class="sxs-lookup"><span data-stu-id="58086-126">This is the same as the previous example.</span></span>

<span data-ttu-id="58086-127">第二個命令會從 $Acl 的 ACL 設定中移除 ID 為0的規則。</span><span class="sxs-lookup"><span data-stu-id="58086-127">The second command removes the rule that has the ID 0 from the ACL configuration in $Acl.</span></span>

<span data-ttu-id="58086-128">最終命令會為虛擬機器設定 ACL 設定物件，並更新該虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="58086-128">The final command sets the ACL configuration object for the virtual machine and updates that virtual machine.</span></span>
<span data-ttu-id="58086-129">這與上一個範例相同。</span><span class="sxs-lookup"><span data-stu-id="58086-129">This is the same as the previous example.</span></span>

## <span data-ttu-id="58086-130">參數</span><span class="sxs-lookup"><span data-stu-id="58086-130">PARAMETERS</span></span>

### <span data-ttu-id="58086-131">-ACL</span><span class="sxs-lookup"><span data-stu-id="58086-131">-ACL</span></span>
<span data-ttu-id="58086-132">指定此 Cmdlet 修改的 ACL 設定物件。</span><span class="sxs-lookup"><span data-stu-id="58086-132">Specifies an ACL configuration object that this cmdlet modifies.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58086-133">-動作</span><span class="sxs-lookup"><span data-stu-id="58086-133">-Action</span></span>
<span data-ttu-id="58086-134">指定此 Cmdlet 新增或修改之規則的動作。</span><span class="sxs-lookup"><span data-stu-id="58086-134">Specifies the action for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="58086-135">有效值為： [允許] 和 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="58086-135">Valid values are: Permit and Deny.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58086-136">-AddRule</span><span class="sxs-lookup"><span data-stu-id="58086-136">-AddRule</span></span>
<span data-ttu-id="58086-137">表示此 Cmdlet 會將規則新增至 ACL 設定。</span><span class="sxs-lookup"><span data-stu-id="58086-137">Indicates that this cmdlet adds a rule to the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58086-138">-描述</span><span class="sxs-lookup"><span data-stu-id="58086-138">-Description</span></span>
<span data-ttu-id="58086-139">指定此 Cmdlet 新增或修改之規則的描述。</span><span class="sxs-lookup"><span data-stu-id="58086-139">Specifies a description for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58086-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="58086-140">-InformationAction</span></span>
<span data-ttu-id="58086-141">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="58086-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="58086-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="58086-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="58086-143">持續</span><span class="sxs-lookup"><span data-stu-id="58086-143">Continue</span></span>
- <span data-ttu-id="58086-144">理會</span><span class="sxs-lookup"><span data-stu-id="58086-144">Ignore</span></span>
- <span data-ttu-id="58086-145">看</span><span class="sxs-lookup"><span data-stu-id="58086-145">Inquire</span></span>
- <span data-ttu-id="58086-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="58086-146">SilentlyContinue</span></span>
- <span data-ttu-id="58086-147">停止</span><span class="sxs-lookup"><span data-stu-id="58086-147">Stop</span></span>
- <span data-ttu-id="58086-148">封存</span><span class="sxs-lookup"><span data-stu-id="58086-148">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58086-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="58086-149">-InformationVariable</span></span>
<span data-ttu-id="58086-150">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="58086-150">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58086-151">-訂單</span><span class="sxs-lookup"><span data-stu-id="58086-151">-Order</span></span>
<span data-ttu-id="58086-152">指定此 Cmdlet 新增或修改之規則的處理順序。</span><span class="sxs-lookup"><span data-stu-id="58086-152">Specifies the processing order for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58086-153">-RemoteSubnet</span><span class="sxs-lookup"><span data-stu-id="58086-153">-RemoteSubnet</span></span>
<span data-ttu-id="58086-154">指定此 Cmdlet 新增或修改之規則的遠端子網。</span><span class="sxs-lookup"><span data-stu-id="58086-154">Specifies the remote subnet for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="58086-155">在無類別域間路由 (CIDR) 格式中指定位址。</span><span class="sxs-lookup"><span data-stu-id="58086-155">Specifies an address in Classless Interdomain Routing (CIDR) format.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58086-156">-RemoveRule</span><span class="sxs-lookup"><span data-stu-id="58086-156">-RemoveRule</span></span>
<span data-ttu-id="58086-157">指示此 Cmdlet 會從 ACL 設定中移除規則。</span><span class="sxs-lookup"><span data-stu-id="58086-157">Indicates that this cmdlet removes a rule from the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58086-158">-RuleId</span><span class="sxs-lookup"><span data-stu-id="58086-158">-RuleId</span></span>
<span data-ttu-id="58086-159">指定此 Cmdlet 針對 ACL 設定移除或修改之規則的識別碼。</span><span class="sxs-lookup"><span data-stu-id="58086-159">Specifies the ID of the rule that this cmdlet removes or modifies for the ACL configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58086-160">-SetRule</span><span class="sxs-lookup"><span data-stu-id="58086-160">-SetRule</span></span>
<span data-ttu-id="58086-161">表示此 Cmdlet 會修改 ACL 設定中的規則。</span><span class="sxs-lookup"><span data-stu-id="58086-161">Indicates that this cmdlet modifies a rule in the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58086-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58086-162">CommonParameters</span></span>
<span data-ttu-id="58086-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58086-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58086-164">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58086-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58086-165">輸入</span><span class="sxs-lookup"><span data-stu-id="58086-165">INPUTS</span></span>

## <span data-ttu-id="58086-166">輸出</span><span class="sxs-lookup"><span data-stu-id="58086-166">OUTPUTS</span></span>

## <span data-ttu-id="58086-167">筆記</span><span class="sxs-lookup"><span data-stu-id="58086-167">NOTES</span></span>

## <span data-ttu-id="58086-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="58086-168">RELATED LINKS</span></span>

[<span data-ttu-id="58086-169">AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="58086-169">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="58086-170">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="58086-170">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="58086-171">新-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="58086-171">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="58086-172">移除-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="58086-172">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="58086-173">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="58086-173">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="58086-174">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="58086-174">Update-AzureVM</span></span>](./Update-AzureVM.md)


