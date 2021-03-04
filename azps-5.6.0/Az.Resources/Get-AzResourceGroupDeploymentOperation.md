---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 06056bd8bf9060a7610b74b8332ff5ab2a4790f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907305"
---
# <span data-ttu-id="77af4-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="77af4-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="77af4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="77af4-102">SYNOPSIS</span></span>
<span data-ttu-id="77af4-103">執行資源群組部署作業</span><span class="sxs-lookup"><span data-stu-id="77af4-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="77af4-104">語法</span><span class="sxs-lookup"><span data-stu-id="77af4-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77af4-105">描述</span><span class="sxs-lookup"><span data-stu-id="77af4-105">DESCRIPTION</span></span>
<span data-ttu-id="77af4-106">**Get-AzResourceGroupDeploymentOperation Cmdlet** 會列出屬於部署一部分的所有作業，可協助識別特定部署失敗的確切作業，並提供有關其詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="77af4-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="77af4-107">它也可以顯示每個部署作業的回應和要求內容。</span><span class="sxs-lookup"><span data-stu-id="77af4-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="77af4-108">這是入口網站部署詳細資料中所提供的相同資訊。</span><span class="sxs-lookup"><span data-stu-id="77af4-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="77af4-109">若要取得要求和回應內容，請透過 **New-AzResourceGroupDeployment** 提交部署時啟用設定。</span><span class="sxs-lookup"><span data-stu-id="77af4-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="77af4-110">它可能會記錄及公開密碼，例如用於資源屬性或 **listKeys** 作業的密碼，然後當您取回部署作業時，會返回這些密碼。</span><span class="sxs-lookup"><span data-stu-id="77af4-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="77af4-111">若要進一步瞭解如何啟用這項設定，請參閱New-AzResourceGroupDeployment ARM 範本部署</span><span class="sxs-lookup"><span data-stu-id="77af4-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="77af4-112">例子</span><span class="sxs-lookup"><span data-stu-id="77af4-112">EXAMPLES</span></span>

### <span data-ttu-id="77af4-113">範例 1：Get1</span><span class="sxs-lookup"><span data-stu-id="77af4-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="77af4-114">在資源群組「測試」下使用名稱「測試」進行部署作業</span><span class="sxs-lookup"><span data-stu-id="77af4-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="77af4-115">參數</span><span class="sxs-lookup"><span data-stu-id="77af4-115">PARAMETERS</span></span>

### <span data-ttu-id="77af4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77af4-116">-DefaultProfile</span></span>
<span data-ttu-id="77af4-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="77af4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77af4-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="77af4-118">-DeploymentName</span></span>
<span data-ttu-id="77af4-119">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="77af4-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77af4-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="77af4-120">-Pre</span></span>
<span data-ttu-id="77af4-121">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="77af4-121">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="77af4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77af4-122">-ResourceGroupName</span></span>
<span data-ttu-id="77af4-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="77af4-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77af4-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77af4-124">-SubscriptionId</span></span>
<span data-ttu-id="77af4-125">這是要使用的訂閱。</span><span class="sxs-lookup"><span data-stu-id="77af4-125">The subscription to use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77af4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77af4-126">CommonParameters</span></span>
<span data-ttu-id="77af4-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="77af4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77af4-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77af4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77af4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="77af4-129">INPUTS</span></span>

### <span data-ttu-id="77af4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="77af4-130">System.String</span></span>

### <span data-ttu-id="77af4-131">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="77af4-131">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="77af4-132">輸出</span><span class="sxs-lookup"><span data-stu-id="77af4-132">OUTPUTS</span></span>

### <span data-ttu-id="77af4-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="77af4-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="77af4-134">筆記</span><span class="sxs-lookup"><span data-stu-id="77af4-134">NOTES</span></span>

## <span data-ttu-id="77af4-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="77af4-135">RELATED LINKS</span></span>
