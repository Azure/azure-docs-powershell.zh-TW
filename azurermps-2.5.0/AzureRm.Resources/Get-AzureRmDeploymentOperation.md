---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeploymentoperation
schema: 2.0.0
ms.openlocfilehash: 2bb5c3823d974dad53045d9283099befd4d60855
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802222"
---
# <span data-ttu-id="7287f-101">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7287f-101">Get-AzureRmDeploymentOperation</span></span>

## <span data-ttu-id="7287f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7287f-102">SYNOPSIS</span></span>
<span data-ttu-id="7287f-103">取得部署作業</span><span class="sxs-lookup"><span data-stu-id="7287f-103">Get deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7287f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7287f-104">SYNTAX</span></span>

### <span data-ttu-id="7287f-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="7287f-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7287f-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="7287f-106">GetByDeploymentObject</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7287f-107">說明</span><span class="sxs-lookup"><span data-stu-id="7287f-107">DESCRIPTION</span></span>
<span data-ttu-id="7287f-108">**AzureRmDeploymentOperation** Cmdlet 會列出部署中的所有作業，以協助您識別並提供有關特定部署失敗之確切作業的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7287f-108">The **Get-AzureRmDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="7287f-109">它也可以顯示每個部署作業的回應和要求內容。</span><span class="sxs-lookup"><span data-stu-id="7287f-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="7287f-110">這與入口網站上的部署詳細資料中提供的資訊相同。</span><span class="sxs-lookup"><span data-stu-id="7287f-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="7287f-111">若要取得要求和回應內容，請在透過 **新的 AzureRmDeployment** 提交部署時啟用此設定。</span><span class="sxs-lookup"><span data-stu-id="7287f-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmDeployment**.</span></span>
<span data-ttu-id="7287f-112">它可能會記錄和公開在您檢索部署作業時傳回的資源屬性或 **listKeys** 作業中所使用的密碼等機密。</span><span class="sxs-lookup"><span data-stu-id="7287f-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="7287f-113">如需此設定及如何啟用的詳細資訊，請參閱 New-AzureRmDeployment 與調試 ARM 範本部署</span><span class="sxs-lookup"><span data-stu-id="7287f-113">For more on this setting and how to enable it, see New-AzureRmDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="7287f-114">示例</span><span class="sxs-lookup"><span data-stu-id="7287f-114">EXAMPLES</span></span>

### <span data-ttu-id="7287f-115">取得給定部署名稱的部署作業</span><span class="sxs-lookup"><span data-stu-id="7287f-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzureRmDeploymentOperation -DeploymentName test
```

<span data-ttu-id="7287f-116">取得目前訂閱範圍中名稱為「test」的部署作業。</span><span class="sxs-lookup"><span data-stu-id="7287f-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="7287f-117">取得部署並取得其部署作業</span><span class="sxs-lookup"><span data-stu-id="7287f-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "test" | Get-AzureRmDeploymentOperation
```

<span data-ttu-id="7287f-118">這個命令會在目前的訂閱範圍中取得「test」部署，並取得其部署作業。</span><span class="sxs-lookup"><span data-stu-id="7287f-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="7287f-119">參數</span><span class="sxs-lookup"><span data-stu-id="7287f-119">PARAMETERS</span></span>

### <span data-ttu-id="7287f-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7287f-120">-ApiVersion</span></span>
<span data-ttu-id="7287f-121">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="7287f-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7287f-122">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="7287f-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="7287f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7287f-123">-DefaultProfile</span></span>
<span data-ttu-id="7287f-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7287f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7287f-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="7287f-125">-DeploymentName</span></span>
<span data-ttu-id="7287f-126">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="7287f-126">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7287f-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="7287f-127">-DeploymentObject</span></span>
<span data-ttu-id="7287f-128">部署物件。</span><span class="sxs-lookup"><span data-stu-id="7287f-128">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7287f-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7287f-129">-OperationId</span></span>
<span data-ttu-id="7287f-130">部署操作 Id。</span><span class="sxs-lookup"><span data-stu-id="7287f-130">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7287f-131">-預先</span><span class="sxs-lookup"><span data-stu-id="7287f-131">-Pre</span></span>
<span data-ttu-id="7287f-132">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="7287f-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7287f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7287f-133">CommonParameters</span></span>
<span data-ttu-id="7287f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7287f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7287f-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7287f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7287f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7287f-136">INPUTS</span></span>

### <span data-ttu-id="7287f-137">System.object</span><span class="sxs-lookup"><span data-stu-id="7287f-137">System.String</span></span>
<span data-ttu-id="7287f-138">系統. Nullable "1 [[System. Guid，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7287f-138">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7287f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7287f-139">OUTPUTS</span></span>

### <span data-ttu-id="7287f-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7287f-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="7287f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7287f-141">NOTES</span></span>

## <span data-ttu-id="7287f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7287f-142">RELATED LINKS</span></span>
