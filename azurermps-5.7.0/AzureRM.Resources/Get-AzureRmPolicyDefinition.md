---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: d9d79374e426c6d895fbfcef957da20ed9721f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453075"
---
# <span data-ttu-id="d8c8d-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d8c8d-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="d8c8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c8d-103">取得原則定義。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8c8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8c8d-104">SYNTAX</span></span>

### <span data-ttu-id="d8c8d-105">GetAllPolicyDefinitions (預設) </span><span class="sxs-lookup"><span data-stu-id="d8c8d-105">GetAllPolicyDefinitions (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d8c8d-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="d8c8d-106">GetByPolicyDefintionName</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d8c8d-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d8c8d-107">GetByPolicyDefinitionId</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d8c8d-108">說明</span><span class="sxs-lookup"><span data-stu-id="d8c8d-108">DESCRIPTION</span></span>
<span data-ttu-id="d8c8d-109">**AzureRmPolicyDefinition** Cmdlet 會取得所有原則定義或由名稱或識別碼所識別的特定原則定義。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-109">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="d8c8d-110">示例</span><span class="sxs-lookup"><span data-stu-id="d8c8d-110">EXAMPLES</span></span>

### <span data-ttu-id="d8c8d-111">範例1：取得所有原則定義</span><span class="sxs-lookup"><span data-stu-id="d8c8d-111">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="d8c8d-112">這個命令會取得所有原則定義。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-112">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="d8c8d-113">範例2：依名稱取得原則定義</span><span class="sxs-lookup"><span data-stu-id="d8c8d-113">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="d8c8d-114">這個命令會取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-114">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="d8c8d-115">參數</span><span class="sxs-lookup"><span data-stu-id="d8c8d-115">PARAMETERS</span></span>

### <span data-ttu-id="d8c8d-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d8c8d-116">-ApiVersion</span></span>
<span data-ttu-id="d8c8d-117">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d8c8d-118">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d8c8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c8d-119">-DefaultProfile</span></span>
<span data-ttu-id="d8c8d-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d8c8d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8c8d-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d8c8d-121">-Id</span></span>
<span data-ttu-id="d8c8d-122">指定此 Cmdlet 所取得之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-122">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d8c8d-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d8c8d-123">-InformationAction</span></span>
<span data-ttu-id="d8c8d-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d8c8d-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d8c8d-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8c8d-126">持續</span><span class="sxs-lookup"><span data-stu-id="d8c8d-126">Continue</span></span>
- <span data-ttu-id="d8c8d-127">理會</span><span class="sxs-lookup"><span data-stu-id="d8c8d-127">Ignore</span></span>
- <span data-ttu-id="d8c8d-128">看</span><span class="sxs-lookup"><span data-stu-id="d8c8d-128">Inquire</span></span>
- <span data-ttu-id="d8c8d-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d8c8d-129">SilentlyContinue</span></span>
- <span data-ttu-id="d8c8d-130">停止</span><span class="sxs-lookup"><span data-stu-id="d8c8d-130">Stop</span></span>
- <span data-ttu-id="d8c8d-131">封存</span><span class="sxs-lookup"><span data-stu-id="d8c8d-131">Suspend</span></span>

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

### <span data-ttu-id="d8c8d-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d8c8d-132">-InformationVariable</span></span>
<span data-ttu-id="d8c8d-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d8c8d-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8c8d-134">-Name</span></span>
<span data-ttu-id="d8c8d-135">指定此 Cmdlet 所取得之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-135">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d8c8d-136">-預先</span><span class="sxs-lookup"><span data-stu-id="d8c8d-136">-Pre</span></span>
<span data-ttu-id="d8c8d-137">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d8c8d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c8d-138">CommonParameters</span></span>
<span data-ttu-id="d8c8d-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c8d-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c8d-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d8c8d-141">INPUTS</span></span>

### <span data-ttu-id="d8c8d-142">所有</span><span class="sxs-lookup"><span data-stu-id="d8c8d-142">None</span></span>
<span data-ttu-id="d8c8d-143">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d8c8d-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8c8d-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d8c8d-144">OUTPUTS</span></span>

### <span data-ttu-id="d8c8d-145">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="d8c8d-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d8c8d-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d8c8d-146">NOTES</span></span>

## <span data-ttu-id="d8c8d-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8c8d-147">RELATED LINKS</span></span>

[<span data-ttu-id="d8c8d-148">新-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d8c8d-148">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d8c8d-149">移除-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d8c8d-149">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d8c8d-150">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d8c8d-150">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


