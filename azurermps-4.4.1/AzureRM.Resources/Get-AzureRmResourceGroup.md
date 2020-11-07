---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 0963d439efd4ab65a2117773cb6b7bb97043972c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624779"
---
# <span data-ttu-id="08cc6-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="08cc6-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="08cc6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="08cc6-103">取得資源群組。</span><span class="sxs-lookup"><span data-stu-id="08cc6-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08cc6-104">句法</span><span class="sxs-lookup"><span data-stu-id="08cc6-104">SYNTAX</span></span>

### <span data-ttu-id="08cc6-105">根據名稱列出資源群組。</span><span class="sxs-lookup"><span data-stu-id="08cc6-105">Lists the resource group based on the name.</span></span> <span data-ttu-id="08cc6-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="08cc6-106">(Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08cc6-107">根據 [識別碼] 列出 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="08cc6-107">Lists the resource group based on the Id.</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08cc6-108">說明</span><span class="sxs-lookup"><span data-stu-id="08cc6-108">DESCRIPTION</span></span>
<span data-ttu-id="08cc6-109">**AzureRmResourceGroup** Cmdlet 會在目前的訂閱中取得 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="08cc6-109">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="08cc6-110">您可以取得所有資源群組，或是依名稱或其他屬性來指定資源群組。</span><span class="sxs-lookup"><span data-stu-id="08cc6-110">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="08cc6-111">根據預設，這個 Cmdlet 會取得目前訂閱中的所有資源群組。</span><span class="sxs-lookup"><span data-stu-id="08cc6-111">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="08cc6-112">如需有關 Azure 資源和 Azure 資源群組的詳細資訊，請參閱 New-AzureRmResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08cc6-112">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="08cc6-113">示例</span><span class="sxs-lookup"><span data-stu-id="08cc6-113">EXAMPLES</span></span>

### <span data-ttu-id="08cc6-114">範例1：依名稱取得資源群組</span><span class="sxs-lookup"><span data-stu-id="08cc6-114">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="08cc6-115">這個命令會在您的訂閱中取得名為 EngineerBlog 的 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="08cc6-115">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="08cc6-116">範例2：取得資源群組的所有標籤</span><span class="sxs-lookup"><span data-stu-id="08cc6-116">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="08cc6-117">這個命令會取得名為 ContosoRG 的資源群組，並顯示與該群組相關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="08cc6-117">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

## <span data-ttu-id="08cc6-118">參數</span><span class="sxs-lookup"><span data-stu-id="08cc6-118">PARAMETERS</span></span>

### <span data-ttu-id="08cc6-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="08cc6-119">-ApiVersion</span></span>
<span data-ttu-id="08cc6-120">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="08cc6-120">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="08cc6-121">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="08cc6-121">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="08cc6-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="08cc6-122">-Id</span></span>
<span data-ttu-id="08cc6-123">指定要取得之資源群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="08cc6-123">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="08cc6-124">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="08cc6-124">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the Id.
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08cc6-125">-位置</span><span class="sxs-lookup"><span data-stu-id="08cc6-125">-Location</span></span>
<span data-ttu-id="08cc6-126">指定要取得之資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="08cc6-126">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="08cc6-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="08cc6-127">-Name</span></span>
<span data-ttu-id="08cc6-128">指定要取得之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="08cc6-128">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="08cc6-129">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="08cc6-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the name.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08cc6-130">-預先</span><span class="sxs-lookup"><span data-stu-id="08cc6-130">-Pre</span></span>
<span data-ttu-id="08cc6-131">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="08cc6-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="08cc6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08cc6-132">-DefaultProfile</span></span>
<span data-ttu-id="08cc6-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08cc6-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08cc6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08cc6-134">CommonParameters</span></span>
<span data-ttu-id="08cc6-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08cc6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08cc6-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08cc6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08cc6-137">輸入</span><span class="sxs-lookup"><span data-stu-id="08cc6-137">INPUTS</span></span>

### <span data-ttu-id="08cc6-138">字串</span><span class="sxs-lookup"><span data-stu-id="08cc6-138">String</span></span>
<span data-ttu-id="08cc6-139">您可以透過屬性名稱將輸入輸送至 Cmdlet，但不能依值進行。</span><span class="sxs-lookup"><span data-stu-id="08cc6-139">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="08cc6-140">輸出</span><span class="sxs-lookup"><span data-stu-id="08cc6-140">OUTPUTS</span></span>

### <span data-ttu-id="08cc6-141">PSResourceGroup 中的 ResourceManagement</span><span class="sxs-lookup"><span data-stu-id="08cc6-141">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="08cc6-142">這個 Cmdlet 會傳回資源群組。</span><span class="sxs-lookup"><span data-stu-id="08cc6-142">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="08cc6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="08cc6-143">NOTES</span></span>

## <span data-ttu-id="08cc6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="08cc6-144">RELATED LINKS</span></span>

[<span data-ttu-id="08cc6-145">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="08cc6-145">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="08cc6-146">移除-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="08cc6-146">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="08cc6-147">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="08cc6-147">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


