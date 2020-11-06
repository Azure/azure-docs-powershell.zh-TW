---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 63ab8e9004b993429af31cb54e360c0b6d9854fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454867"
---
# <span data-ttu-id="55e17-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="55e17-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="55e17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55e17-102">SYNOPSIS</span></span>
<span data-ttu-id="55e17-103">取得原則定義。</span><span class="sxs-lookup"><span data-stu-id="55e17-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55e17-104">句法</span><span class="sxs-lookup"><span data-stu-id="55e17-104">SYNTAX</span></span>

### <span data-ttu-id="55e17-105">清單所有原則定義參數已設定。</span><span class="sxs-lookup"><span data-stu-id="55e17-105">The list all policy definitions parameter set.</span></span> <span data-ttu-id="55e17-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="55e17-106">(Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="55e17-107">原則定義名稱參數已設定。</span><span class="sxs-lookup"><span data-stu-id="55e17-107">The policy definition name parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="55e17-108">已設定原則定義識別碼參數。</span><span class="sxs-lookup"><span data-stu-id="55e17-108">The policy definition Id parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="55e17-109">說明</span><span class="sxs-lookup"><span data-stu-id="55e17-109">DESCRIPTION</span></span>
<span data-ttu-id="55e17-110">**AzureRmPolicyDefinition** Cmdlet 會取得所有原則定義或由名稱或識別碼所識別的特定原則定義。</span><span class="sxs-lookup"><span data-stu-id="55e17-110">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="55e17-111">示例</span><span class="sxs-lookup"><span data-stu-id="55e17-111">EXAMPLES</span></span>

### <span data-ttu-id="55e17-112">範例1：取得所有原則定義</span><span class="sxs-lookup"><span data-stu-id="55e17-112">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="55e17-113">這個命令會取得所有原則定義。</span><span class="sxs-lookup"><span data-stu-id="55e17-113">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="55e17-114">範例2：依名稱取得原則定義</span><span class="sxs-lookup"><span data-stu-id="55e17-114">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="55e17-115">這個命令會取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="55e17-115">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="55e17-116">參數</span><span class="sxs-lookup"><span data-stu-id="55e17-116">PARAMETERS</span></span>

### <span data-ttu-id="55e17-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="55e17-117">-ApiVersion</span></span>
<span data-ttu-id="55e17-118">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="55e17-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="55e17-119">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="55e17-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="55e17-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="55e17-120">-Id</span></span>
<span data-ttu-id="55e17-121">指定此 Cmdlet 所取得之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="55e17-121">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55e17-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="55e17-122">-InformationAction</span></span>
<span data-ttu-id="55e17-123">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="55e17-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="55e17-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="55e17-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55e17-125">持續</span><span class="sxs-lookup"><span data-stu-id="55e17-125">Continue</span></span>
- <span data-ttu-id="55e17-126">理會</span><span class="sxs-lookup"><span data-stu-id="55e17-126">Ignore</span></span>
- <span data-ttu-id="55e17-127">看</span><span class="sxs-lookup"><span data-stu-id="55e17-127">Inquire</span></span>
- <span data-ttu-id="55e17-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="55e17-128">SilentlyContinue</span></span>
- <span data-ttu-id="55e17-129">停止</span><span class="sxs-lookup"><span data-stu-id="55e17-129">Stop</span></span>
- <span data-ttu-id="55e17-130">封存</span><span class="sxs-lookup"><span data-stu-id="55e17-130">Suspend</span></span>

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

### <span data-ttu-id="55e17-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="55e17-131">-InformationVariable</span></span>
<span data-ttu-id="55e17-132">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="55e17-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="55e17-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="55e17-133">-Name</span></span>
<span data-ttu-id="55e17-134">指定此 Cmdlet 所取得之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="55e17-134">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55e17-135">-預先</span><span class="sxs-lookup"><span data-stu-id="55e17-135">-Pre</span></span>
<span data-ttu-id="55e17-136">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="55e17-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="55e17-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e17-137">-DefaultProfile</span></span>
<span data-ttu-id="55e17-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55e17-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55e17-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e17-139">CommonParameters</span></span>
<span data-ttu-id="55e17-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55e17-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e17-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55e17-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e17-142">輸入</span><span class="sxs-lookup"><span data-stu-id="55e17-142">INPUTS</span></span>

## <span data-ttu-id="55e17-143">輸出</span><span class="sxs-lookup"><span data-stu-id="55e17-143">OUTPUTS</span></span>

### <span data-ttu-id="55e17-144">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="55e17-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="55e17-145">筆記</span><span class="sxs-lookup"><span data-stu-id="55e17-145">NOTES</span></span>

## <span data-ttu-id="55e17-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="55e17-146">RELATED LINKS</span></span>

[<span data-ttu-id="55e17-147">新-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="55e17-147">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="55e17-148">移除-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="55e17-148">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="55e17-149">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="55e17-149">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


