---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: be045303db770cbba919d27ed9563aa64283572c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915569"
---
# <span data-ttu-id="6247f-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6247f-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="6247f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6247f-102">SYNOPSIS</span></span>
<span data-ttu-id="6247f-103">登入 Azure 容器登錄。</span><span class="sxs-lookup"><span data-stu-id="6247f-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="6247f-104">語法</span><span class="sxs-lookup"><span data-stu-id="6247f-104">SYNTAX</span></span>

### <span data-ttu-id="6247f-105">WithoutNameAndPasswordParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6247f-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6247f-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="6247f-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6247f-107">描述</span><span class="sxs-lookup"><span data-stu-id="6247f-107">DESCRIPTION</span></span>
<span data-ttu-id="6247f-108">登入 Azure 容器登錄。</span><span class="sxs-lookup"><span data-stu-id="6247f-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="6247f-109">例子</span><span class="sxs-lookup"><span data-stu-id="6247f-109">EXAMPLES</span></span>

### <span data-ttu-id="6247f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="6247f-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="6247f-111">在已登入 Azure 帳戶時，無需認證就登入 ACR。</span><span class="sxs-lookup"><span data-stu-id="6247f-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="6247f-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="6247f-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="6247f-113">啟用系統管理員使用者時，使用系統管理員使用者名稱/密碼登入 ACR。</span><span class="sxs-lookup"><span data-stu-id="6247f-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="6247f-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="6247f-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="6247f-115">使用服務主體應用程式識別碼和密碼登入 ACR。</span><span class="sxs-lookup"><span data-stu-id="6247f-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="6247f-116">參數</span><span class="sxs-lookup"><span data-stu-id="6247f-116">PARAMETERS</span></span>

### <span data-ttu-id="6247f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6247f-117">-DefaultProfile</span></span>
<span data-ttu-id="6247f-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6247f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6247f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6247f-119">-Name</span></span>
<span data-ttu-id="6247f-120">Azure 容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="6247f-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6247f-121">-密碼</span><span class="sxs-lookup"><span data-stu-id="6247f-121">-Password</span></span>
<span data-ttu-id="6247f-122">Azure 容器登錄的密碼。</span><span class="sxs-lookup"><span data-stu-id="6247f-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6247f-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="6247f-123">-UserName</span></span>
<span data-ttu-id="6247f-124">Azure 容器登錄的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="6247f-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6247f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6247f-125">CommonParameters</span></span>
<span data-ttu-id="6247f-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6247f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6247f-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6247f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6247f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="6247f-128">INPUTS</span></span>

### <span data-ttu-id="6247f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6247f-129">System.String</span></span>

## <span data-ttu-id="6247f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="6247f-130">OUTPUTS</span></span>

### <span data-ttu-id="6247f-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6247f-131">System.Boolean</span></span>

## <span data-ttu-id="6247f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="6247f-132">NOTES</span></span>

## <span data-ttu-id="6247f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="6247f-133">RELATED LINKS</span></span>
