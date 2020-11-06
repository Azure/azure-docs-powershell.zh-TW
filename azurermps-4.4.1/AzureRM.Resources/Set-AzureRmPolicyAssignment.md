---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: fcb1283531b35365cc8c07016c839a1152011160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447999"
---
# <span data-ttu-id="eac10-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="eac10-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="eac10-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eac10-102">SYNOPSIS</span></span>
<span data-ttu-id="eac10-103">修改原則分派。</span><span class="sxs-lookup"><span data-stu-id="eac10-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eac10-104">句法</span><span class="sxs-lookup"><span data-stu-id="eac10-104">SYNTAX</span></span>

### <span data-ttu-id="eac10-105">原則指派名稱參數已設定。</span><span class="sxs-lookup"><span data-stu-id="eac10-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="eac10-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="eac10-106">(Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="eac10-107">原則指派識別碼參數已設定。</span><span class="sxs-lookup"><span data-stu-id="eac10-107">The policy assignment Id parameter set.</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eac10-108">說明</span><span class="sxs-lookup"><span data-stu-id="eac10-108">DESCRIPTION</span></span>
<span data-ttu-id="eac10-109">**AzureRmPolicyAssignment** Cmdlet 會修改原則指派。</span><span class="sxs-lookup"><span data-stu-id="eac10-109">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="eac10-110">依識別碼或名稱和範圍指定作業。</span><span class="sxs-lookup"><span data-stu-id="eac10-110">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="eac10-111">示例</span><span class="sxs-lookup"><span data-stu-id="eac10-111">EXAMPLES</span></span>

### <span data-ttu-id="eac10-112">範例1：更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="eac10-112">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="eac10-113">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="eac10-113">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="eac10-114">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="eac10-114">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="eac10-115">第二個命令會使用 Get-AzureRmPolicyAssignment Cmdlet 來取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="eac10-115">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="eac10-116">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="eac10-116">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="eac10-117">Final 命令會更新由 $PolicyAssignment 的 **ResourceId** 屬性所識別之原則指派的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="eac10-117">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="eac10-118">參數</span><span class="sxs-lookup"><span data-stu-id="eac10-118">PARAMETERS</span></span>

### <span data-ttu-id="eac10-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eac10-119">-ApiVersion</span></span>
<span data-ttu-id="eac10-120">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="eac10-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="eac10-121">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="eac10-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="eac10-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eac10-122">-DisplayName</span></span>
<span data-ttu-id="eac10-123">指定原則指派的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="eac10-123">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac10-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="eac10-124">-Id</span></span>
<span data-ttu-id="eac10-125">指定此 Cmdlet 所修改之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="eac10-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac10-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="eac10-126">-InformationAction</span></span>
<span data-ttu-id="eac10-127">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="eac10-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eac10-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="eac10-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eac10-129">持續</span><span class="sxs-lookup"><span data-stu-id="eac10-129">Continue</span></span>
- <span data-ttu-id="eac10-130">理會</span><span class="sxs-lookup"><span data-stu-id="eac10-130">Ignore</span></span>
- <span data-ttu-id="eac10-131">看</span><span class="sxs-lookup"><span data-stu-id="eac10-131">Inquire</span></span>
- <span data-ttu-id="eac10-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eac10-132">SilentlyContinue</span></span>
- <span data-ttu-id="eac10-133">停止</span><span class="sxs-lookup"><span data-stu-id="eac10-133">Stop</span></span>
- <span data-ttu-id="eac10-134">封存</span><span class="sxs-lookup"><span data-stu-id="eac10-134">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac10-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eac10-135">-InformationVariable</span></span>
<span data-ttu-id="eac10-136">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="eac10-136">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac10-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="eac10-137">-Name</span></span>
<span data-ttu-id="eac10-138">指定此 Cmdlet 所修改之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="eac10-138">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac10-139">-NotScope</span><span class="sxs-lookup"><span data-stu-id="eac10-139">-NotScope</span></span>
<span data-ttu-id="eac10-140">原則指派不是作用中的範圍。</span><span class="sxs-lookup"><span data-stu-id="eac10-140">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac10-141">-預先</span><span class="sxs-lookup"><span data-stu-id="eac10-141">-Pre</span></span>
<span data-ttu-id="eac10-142">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="eac10-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="eac10-143">-範圍</span><span class="sxs-lookup"><span data-stu-id="eac10-143">-Scope</span></span>
<span data-ttu-id="eac10-144">指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="eac10-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac10-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac10-145">-DefaultProfile</span></span>
<span data-ttu-id="eac10-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eac10-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eac10-147">-描述</span><span class="sxs-lookup"><span data-stu-id="eac10-147">-Description</span></span>
<span data-ttu-id="eac10-148">原則指派的描述。</span><span class="sxs-lookup"><span data-stu-id="eac10-148">The description for policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac10-149">-Sku</span><span class="sxs-lookup"><span data-stu-id="eac10-149">-Sku</span></span>
<span data-ttu-id="eac10-150">代表 sku 屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="eac10-150">A hash table which represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac10-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac10-151">CommonParameters</span></span>
<span data-ttu-id="eac10-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eac10-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac10-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eac10-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac10-154">輸入</span><span class="sxs-lookup"><span data-stu-id="eac10-154">INPUTS</span></span>

## <span data-ttu-id="eac10-155">輸出</span><span class="sxs-lookup"><span data-stu-id="eac10-155">OUTPUTS</span></span>

### <span data-ttu-id="eac10-156">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="eac10-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="eac10-157">筆記</span><span class="sxs-lookup"><span data-stu-id="eac10-157">NOTES</span></span>

## <span data-ttu-id="eac10-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="eac10-158">RELATED LINKS</span></span>

[<span data-ttu-id="eac10-159">AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="eac10-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="eac10-160">新-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="eac10-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="eac10-161">移除-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="eac10-161">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


