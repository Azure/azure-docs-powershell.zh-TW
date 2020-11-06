---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: d7e01294836145b09844fa3bca49421df20f67d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453056"
---
# <span data-ttu-id="b6883-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b6883-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="b6883-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6883-102">SYNOPSIS</span></span>
<span data-ttu-id="b6883-103">修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="b6883-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6883-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6883-104">SYNTAX</span></span>

### <span data-ttu-id="b6883-105">SetByPolicyDefinitionName (預設) </span><span class="sxs-lookup"><span data-stu-id="b6883-105">SetByPolicyDefinitionName (Default)</span></span>
```
Set-AzureRmPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b6883-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="b6883-106">GetByPolicyDefintionName</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b6883-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b6883-107">GetByPolicyDefinitionId</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b6883-108">說明</span><span class="sxs-lookup"><span data-stu-id="b6883-108">DESCRIPTION</span></span>
<span data-ttu-id="b6883-109">**AzureRmPolicyDefinition** Cmdlet 會修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="b6883-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="b6883-110">示例</span><span class="sxs-lookup"><span data-stu-id="b6883-110">EXAMPLES</span></span>

### <span data-ttu-id="b6883-111">範例1：更新原則定義的描述</span><span class="sxs-lookup"><span data-stu-id="b6883-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="b6883-112">第一個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="b6883-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="b6883-113">該命令會將該物件儲存在 $PolicyDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="b6883-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="b6883-114">第二個命令會更新 $PolicyDefinition 的 **ResourceId** 屬性所識別之原則定義的描述。</span><span class="sxs-lookup"><span data-stu-id="b6883-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="b6883-115">參數</span><span class="sxs-lookup"><span data-stu-id="b6883-115">PARAMETERS</span></span>

### <span data-ttu-id="b6883-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b6883-116">-ApiVersion</span></span>
<span data-ttu-id="b6883-117">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b6883-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b6883-118">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="b6883-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6883-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6883-119">-DefaultProfile</span></span>
<span data-ttu-id="b6883-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b6883-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6883-121">-描述</span><span class="sxs-lookup"><span data-stu-id="b6883-121">-Description</span></span>
<span data-ttu-id="b6883-122">指定原則定義的新描述。</span><span class="sxs-lookup"><span data-stu-id="b6883-122">Specifies a new description for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6883-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b6883-123">-DisplayName</span></span>
<span data-ttu-id="b6883-124">指定原則定義的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b6883-124">Specifies a new display name for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6883-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b6883-125">-Id</span></span>
<span data-ttu-id="b6883-126">指定此 Cmdlet 所修改之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6883-126">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6883-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b6883-127">-InformationAction</span></span>
<span data-ttu-id="b6883-128">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b6883-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b6883-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b6883-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6883-130">持續</span><span class="sxs-lookup"><span data-stu-id="b6883-130">Continue</span></span>
- <span data-ttu-id="b6883-131">理會</span><span class="sxs-lookup"><span data-stu-id="b6883-131">Ignore</span></span>
- <span data-ttu-id="b6883-132">看</span><span class="sxs-lookup"><span data-stu-id="b6883-132">Inquire</span></span>
- <span data-ttu-id="b6883-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b6883-133">SilentlyContinue</span></span>
- <span data-ttu-id="b6883-134">停止</span><span class="sxs-lookup"><span data-stu-id="b6883-134">Stop</span></span>
- <span data-ttu-id="b6883-135">封存</span><span class="sxs-lookup"><span data-stu-id="b6883-135">Suspend</span></span>

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

### <span data-ttu-id="b6883-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b6883-136">-InformationVariable</span></span>
<span data-ttu-id="b6883-137">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b6883-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b6883-138">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="b6883-138">-Metadata</span></span>
<span data-ttu-id="b6883-139">原則定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b6883-139">The metadata for policy definition.</span></span> <span data-ttu-id="b6883-140">這可以是包含中繼資料之檔案名的路徑，或以字串形式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b6883-140">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6883-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6883-141">-Name</span></span>
<span data-ttu-id="b6883-142">指定此 Cmdlet 所修改之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6883-142">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6883-143">-參數</span><span class="sxs-lookup"><span data-stu-id="b6883-143">-Parameter</span></span>
<span data-ttu-id="b6883-144">原則定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="b6883-144">The parameters declaration for policy definition.</span></span> <span data-ttu-id="b6883-145">這可以是包含參數宣告之檔案名或 uri 的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="b6883-145">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6883-146">-原則</span><span class="sxs-lookup"><span data-stu-id="b6883-146">-Policy</span></span>
<span data-ttu-id="b6883-147">指定原則定義的新原則規則。</span><span class="sxs-lookup"><span data-stu-id="b6883-147">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="b6883-148">您可以指定 json 檔案的路徑，或是包含 JavaScript 物件符號 (JSON) 格式之原則的字串。</span><span class="sxs-lookup"><span data-stu-id="b6883-148">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6883-149">-預先</span><span class="sxs-lookup"><span data-stu-id="b6883-149">-Pre</span></span>
<span data-ttu-id="b6883-150">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b6883-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6883-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6883-151">CommonParameters</span></span>
<span data-ttu-id="b6883-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6883-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6883-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6883-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6883-154">輸入</span><span class="sxs-lookup"><span data-stu-id="b6883-154">INPUTS</span></span>

### <span data-ttu-id="b6883-155">所有</span><span class="sxs-lookup"><span data-stu-id="b6883-155">None</span></span>
<span data-ttu-id="b6883-156">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b6883-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6883-157">輸出</span><span class="sxs-lookup"><span data-stu-id="b6883-157">OUTPUTS</span></span>

### <span data-ttu-id="b6883-158">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="b6883-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b6883-159">筆記</span><span class="sxs-lookup"><span data-stu-id="b6883-159">NOTES</span></span>

## <span data-ttu-id="b6883-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6883-160">RELATED LINKS</span></span>

[<span data-ttu-id="b6883-161">AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b6883-161">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="b6883-162">新-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b6883-162">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="b6883-163">移除-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b6883-163">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


