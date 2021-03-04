---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 5507e180d5f56b75006f31f9cc6753f50d821a3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907325"
---
# <span data-ttu-id="c2b1b-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c2b1b-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="c2b1b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c2b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b1b-103">取得部署作業</span><span class="sxs-lookup"><span data-stu-id="c2b1b-103">Get deployment operation</span></span>

## <span data-ttu-id="c2b1b-104">語法</span><span class="sxs-lookup"><span data-stu-id="c2b1b-104">SYNTAX</span></span>

### <span data-ttu-id="c2b1b-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="c2b1b-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2b1b-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c2b1b-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2b1b-107">描述</span><span class="sxs-lookup"><span data-stu-id="c2b1b-107">DESCRIPTION</span></span>
<span data-ttu-id="c2b1b-108">**Get-AzDeploymentOperation Cmdlet** 會列出屬於部署的所有作業，可協助識別特定部署失敗的確切作業，並提供有關其詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="c2b1b-109">它也可以顯示每個部署作業的回應和要求內容。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="c2b1b-110">這是入口網站部署詳細資料中所提供的相同資訊。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="c2b1b-111">若要取得要求和回應內容，請透過 **New-AzDeployment** 提交部署時啟用設定。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="c2b1b-112">它可能會記錄及公開密碼，例如用於資源屬性或 **listKeys** 作業的密碼，然後當您取回部署作業時，會返回這些密碼。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="c2b1b-113">若要進一步瞭解如何啟用這項設定，請參閱New-AzDeployment ARM 範本部署</span><span class="sxs-lookup"><span data-stu-id="c2b1b-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="c2b1b-114">例子</span><span class="sxs-lookup"><span data-stu-id="c2b1b-114">EXAMPLES</span></span>

### <span data-ttu-id="c2b1b-115">範例 1：取得指定部署名稱的部署作業</span><span class="sxs-lookup"><span data-stu-id="c2b1b-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="c2b1b-116">使用目前訂閱範圍中的名稱「測試」來執行部署作業。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="c2b1b-117">範例 2：取得部署並取得其部署作業</span><span class="sxs-lookup"><span data-stu-id="c2b1b-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="c2b1b-118">此命令會取得目前訂閱範圍中的部署「測試」，並取得其部署作業。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="c2b1b-119">參數</span><span class="sxs-lookup"><span data-stu-id="c2b1b-119">PARAMETERS</span></span>

### <span data-ttu-id="c2b1b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b1b-120">-DefaultProfile</span></span>
<span data-ttu-id="c2b1b-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b1b-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="c2b1b-122">-DeploymentName</span></span>
<span data-ttu-id="c2b1b-123">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-123">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b1b-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c2b1b-124">-DeploymentObject</span></span>
<span data-ttu-id="c2b1b-125">部署物件。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-125">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b1b-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c2b1b-126">-OperationId</span></span>
<span data-ttu-id="c2b1b-127">部署作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-127">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b1b-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="c2b1b-128">-Pre</span></span>
<span data-ttu-id="c2b1b-129">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c2b1b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b1b-130">CommonParameters</span></span>
<span data-ttu-id="c2b1b-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c2b1b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b1b-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2b1b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b1b-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c2b1b-133">INPUTS</span></span>

### <span data-ttu-id="c2b1b-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c2b1b-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c2b1b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c2b1b-135">OUTPUTS</span></span>

### <span data-ttu-id="c2b1b-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c2b1b-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="c2b1b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c2b1b-137">NOTES</span></span>

## <span data-ttu-id="c2b1b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2b1b-138">RELATED LINKS</span></span>
