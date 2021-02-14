---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 3c702d0572bb8e5bdf41deff599b9da6c5cc2dcf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143314"
---
# <span data-ttu-id="f2a24-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f2a24-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="f2a24-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2a24-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a24-103">登入 azure 容器註冊。</span><span class="sxs-lookup"><span data-stu-id="f2a24-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="f2a24-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2a24-104">SYNTAX</span></span>

### <span data-ttu-id="f2a24-105">WithoutNameAndPasswordParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f2a24-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2a24-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2a24-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2a24-107">說明</span><span class="sxs-lookup"><span data-stu-id="f2a24-107">DESCRIPTION</span></span>
<span data-ttu-id="f2a24-108">登入 azure 容器註冊。</span><span class="sxs-lookup"><span data-stu-id="f2a24-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="f2a24-109">示例</span><span class="sxs-lookup"><span data-stu-id="f2a24-109">EXAMPLES</span></span>

### <span data-ttu-id="f2a24-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f2a24-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="f2a24-111">在已登入 azure 帳戶時，登入 [沒有認證的 ACR]。</span><span class="sxs-lookup"><span data-stu-id="f2a24-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="f2a24-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f2a24-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="f2a24-113">在已啟用管理員使用者的情況中，使用系統管理員的使用者名稱登入 ACR。</span><span class="sxs-lookup"><span data-stu-id="f2a24-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="f2a24-114">範例3</span><span class="sxs-lookup"><span data-stu-id="f2a24-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="f2a24-115">使用服務主體應用程式識別碼和密碼登入 ACR。</span><span class="sxs-lookup"><span data-stu-id="f2a24-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="f2a24-116">參數</span><span class="sxs-lookup"><span data-stu-id="f2a24-116">PARAMETERS</span></span>

### <span data-ttu-id="f2a24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a24-117">-DefaultProfile</span></span>
<span data-ttu-id="f2a24-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2a24-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2a24-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2a24-119">-Name</span></span>
<span data-ttu-id="f2a24-120">Azure 容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="f2a24-120">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="f2a24-121">-Password</span><span class="sxs-lookup"><span data-stu-id="f2a24-121">-Password</span></span>
<span data-ttu-id="f2a24-122">Azure 容器註冊的密碼。</span><span class="sxs-lookup"><span data-stu-id="f2a24-122">Password For Azure Container Registry.</span></span>

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

### <span data-ttu-id="f2a24-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="f2a24-123">-UserName</span></span>
<span data-ttu-id="f2a24-124">Azure 容器註冊的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="f2a24-124">User Name For Azure Container Registry.</span></span>

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

### <span data-ttu-id="f2a24-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a24-125">CommonParameters</span></span>
<span data-ttu-id="f2a24-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2a24-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a24-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f2a24-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a24-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f2a24-128">INPUTS</span></span>

### <span data-ttu-id="f2a24-129">System.object</span><span class="sxs-lookup"><span data-stu-id="f2a24-129">System.String</span></span>

## <span data-ttu-id="f2a24-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f2a24-130">OUTPUTS</span></span>

### <span data-ttu-id="f2a24-131">System.object</span><span class="sxs-lookup"><span data-stu-id="f2a24-131">System.Boolean</span></span>

## <span data-ttu-id="f2a24-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f2a24-132">NOTES</span></span>

## <span data-ttu-id="f2a24-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2a24-133">RELATED LINKS</span></span>
