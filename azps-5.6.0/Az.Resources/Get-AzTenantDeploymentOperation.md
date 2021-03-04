---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: cf48e14ded4dd227cb241a341339861bae3a269a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913681"
---
# <span data-ttu-id="66898-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="66898-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="66898-102">簡介</span><span class="sxs-lookup"><span data-stu-id="66898-102">SYNOPSIS</span></span>
<span data-ttu-id="66898-103">在租使用者範圍中取得部署作業</span><span class="sxs-lookup"><span data-stu-id="66898-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="66898-104">語法</span><span class="sxs-lookup"><span data-stu-id="66898-104">SYNTAX</span></span>

### <span data-ttu-id="66898-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="66898-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66898-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="66898-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66898-107">描述</span><span class="sxs-lookup"><span data-stu-id="66898-107">DESCRIPTION</span></span>
<span data-ttu-id="66898-108">**Get-AzTenantDeploymentOperation Cmdlet** 會列出目前租使用者範圍中屬於部署一部分的所有作業，可協助識別特定部署失敗的確切作業，並提供有關其詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="66898-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="66898-109">例子</span><span class="sxs-lookup"><span data-stu-id="66898-109">EXAMPLES</span></span>

### <span data-ttu-id="66898-110">範例 1：取得指定部署名稱的部署作業</span><span class="sxs-lookup"><span data-stu-id="66898-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="66898-111">在目前的租使用者範圍中，使用名稱 "Deploy01" 進行部署作業。</span><span class="sxs-lookup"><span data-stu-id="66898-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="66898-112">範例 2：取得部署並取得其部署作業</span><span class="sxs-lookup"><span data-stu-id="66898-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="66898-113">此命令會取得目前租使用者範圍中的部署「部署01」，並取得其部署作業。</span><span class="sxs-lookup"><span data-stu-id="66898-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="66898-114">參數</span><span class="sxs-lookup"><span data-stu-id="66898-114">PARAMETERS</span></span>

### <span data-ttu-id="66898-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66898-115">-DefaultProfile</span></span>
<span data-ttu-id="66898-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="66898-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66898-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="66898-117">-DeploymentName</span></span>
<span data-ttu-id="66898-118">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="66898-118">The deployment name.</span></span>

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

### <span data-ttu-id="66898-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="66898-119">-DeploymentObject</span></span>
<span data-ttu-id="66898-120">部署物件。</span><span class="sxs-lookup"><span data-stu-id="66898-120">The deployment object.</span></span>

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

### <span data-ttu-id="66898-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="66898-121">-OperationId</span></span>
<span data-ttu-id="66898-122">部署作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="66898-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="66898-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="66898-123">-Pre</span></span>
<span data-ttu-id="66898-124">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="66898-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="66898-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66898-125">CommonParameters</span></span>
<span data-ttu-id="66898-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="66898-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66898-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66898-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66898-128">輸入</span><span class="sxs-lookup"><span data-stu-id="66898-128">INPUTS</span></span>

### <span data-ttu-id="66898-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="66898-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="66898-130">輸出</span><span class="sxs-lookup"><span data-stu-id="66898-130">OUTPUTS</span></span>

### <span data-ttu-id="66898-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="66898-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="66898-132">筆記</span><span class="sxs-lookup"><span data-stu-id="66898-132">NOTES</span></span>

## <span data-ttu-id="66898-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="66898-133">RELATED LINKS</span></span>
