---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435536"
---
# <span data-ttu-id="1dfff-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1dfff-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="1dfff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1dfff-102">SYNOPSIS</span></span>
<span data-ttu-id="1dfff-103">取得部署作業</span><span class="sxs-lookup"><span data-stu-id="1dfff-103">Get deployment operation</span></span>

## <span data-ttu-id="1dfff-104">句法</span><span class="sxs-lookup"><span data-stu-id="1dfff-104">SYNTAX</span></span>

### <span data-ttu-id="1dfff-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="1dfff-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dfff-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1dfff-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dfff-107">說明</span><span class="sxs-lookup"><span data-stu-id="1dfff-107">DESCRIPTION</span></span>
<span data-ttu-id="1dfff-108">**AzDeploymentOperation** Cmdlet 會列出部署中的所有作業，以協助您識別並提供有關特定部署失敗之確切作業的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1dfff-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="1dfff-109">它也可以顯示每個部署作業的回應和要求內容。</span><span class="sxs-lookup"><span data-stu-id="1dfff-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="1dfff-110">這與入口網站上的部署詳細資料中提供的資訊相同。</span><span class="sxs-lookup"><span data-stu-id="1dfff-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="1dfff-111">若要取得要求和回應內容，請在透過 **新的 AzDeployment** 提交部署時啟用此設定。</span><span class="sxs-lookup"><span data-stu-id="1dfff-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="1dfff-112">它可能會記錄和公開在您檢索部署作業時傳回的資源屬性或 **listKeys** 作業中所使用的密碼等機密。</span><span class="sxs-lookup"><span data-stu-id="1dfff-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="1dfff-113">如需此設定及如何啟用的詳細資訊，請參閱 New-AzDeployment 與調試 ARM 範本部署</span><span class="sxs-lookup"><span data-stu-id="1dfff-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="1dfff-114">示例</span><span class="sxs-lookup"><span data-stu-id="1dfff-114">EXAMPLES</span></span>

### <span data-ttu-id="1dfff-115">範例1：取得給定部署名稱的部署作業</span><span class="sxs-lookup"><span data-stu-id="1dfff-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="1dfff-116">取得目前訂閱範圍中名稱為「test」的部署作業。</span><span class="sxs-lookup"><span data-stu-id="1dfff-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="1dfff-117">範例2：取得部署並取得其部署作業</span><span class="sxs-lookup"><span data-stu-id="1dfff-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="1dfff-118">這個命令會在目前的訂閱範圍中取得「test」部署，並取得其部署作業。</span><span class="sxs-lookup"><span data-stu-id="1dfff-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="1dfff-119">參數</span><span class="sxs-lookup"><span data-stu-id="1dfff-119">PARAMETERS</span></span>

### <span data-ttu-id="1dfff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dfff-120">-DefaultProfile</span></span>
<span data-ttu-id="1dfff-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dfff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dfff-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="1dfff-122">-DeploymentName</span></span>
<span data-ttu-id="1dfff-123">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="1dfff-123">The deployment name.</span></span>

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

### <span data-ttu-id="1dfff-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1dfff-124">-DeploymentObject</span></span>
<span data-ttu-id="1dfff-125">部署物件。</span><span class="sxs-lookup"><span data-stu-id="1dfff-125">The deployment object.</span></span>

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

### <span data-ttu-id="1dfff-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="1dfff-126">-OperationId</span></span>
<span data-ttu-id="1dfff-127">部署操作 Id。</span><span class="sxs-lookup"><span data-stu-id="1dfff-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="1dfff-128">-預先</span><span class="sxs-lookup"><span data-stu-id="1dfff-128">-Pre</span></span>
<span data-ttu-id="1dfff-129">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="1dfff-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1dfff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dfff-130">CommonParameters</span></span>
<span data-ttu-id="1dfff-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1dfff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dfff-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1dfff-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dfff-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1dfff-133">INPUTS</span></span>

### <span data-ttu-id="1dfff-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1dfff-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1dfff-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1dfff-135">OUTPUTS</span></span>

### <span data-ttu-id="1dfff-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1dfff-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="1dfff-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1dfff-137">NOTES</span></span>

## <span data-ttu-id="1dfff-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dfff-138">RELATED LINKS</span></span>
