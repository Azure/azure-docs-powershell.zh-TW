---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 22feec8308b682aa2290de6bd8b7361bb07cd560
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623118"
---
# <span data-ttu-id="4254b-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4254b-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="4254b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4254b-102">SYNOPSIS</span></span>
<span data-ttu-id="4254b-103">建立 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="4254b-103">Creates an API management group.</span></span>

## <span data-ttu-id="4254b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4254b-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4254b-105">說明</span><span class="sxs-lookup"><span data-stu-id="4254b-105">DESCRIPTION</span></span>
<span data-ttu-id="4254b-106">**新的-AzApiManagementGroup** Cmdlet 會建立 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="4254b-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="4254b-107">示例</span><span class="sxs-lookup"><span data-stu-id="4254b-107">EXAMPLES</span></span>

### <span data-ttu-id="4254b-108">範例1：建立管理群組</span><span class="sxs-lookup"><span data-stu-id="4254b-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="4254b-109">這個命令會建立管理群組。</span><span class="sxs-lookup"><span data-stu-id="4254b-109">This command creates a management group.</span></span>

## <span data-ttu-id="4254b-110">參數</span><span class="sxs-lookup"><span data-stu-id="4254b-110">PARAMETERS</span></span>

### <span data-ttu-id="4254b-111">-內容</span><span class="sxs-lookup"><span data-stu-id="4254b-111">-Context</span></span>
<span data-ttu-id="4254b-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="4254b-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4254b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4254b-113">-DefaultProfile</span></span>
<span data-ttu-id="4254b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4254b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4254b-115">-描述</span><span class="sxs-lookup"><span data-stu-id="4254b-115">-Description</span></span>
<span data-ttu-id="4254b-116">指定管理群組的描述。</span><span class="sxs-lookup"><span data-stu-id="4254b-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="4254b-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="4254b-117">-ExternalId</span></span>
<span data-ttu-id="4254b-118">對於外部群組，此屬性包含來自外部身分識別提供者的群組識別碼，例如 Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c;否則，該值為 null。</span><span class="sxs-lookup"><span data-stu-id="4254b-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="4254b-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="4254b-119">-GroupId</span></span>
<span data-ttu-id="4254b-120">指定新管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4254b-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="4254b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4254b-121">-Name</span></span>
<span data-ttu-id="4254b-122">指定管理組名。</span><span class="sxs-lookup"><span data-stu-id="4254b-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="4254b-123">-類型</span><span class="sxs-lookup"><span data-stu-id="4254b-123">-Type</span></span>
<span data-ttu-id="4254b-124">群組類型。</span><span class="sxs-lookup"><span data-stu-id="4254b-124">Group Type.</span></span> <span data-ttu-id="4254b-125">[自訂群組] 是 [使用者定義] 群組。</span><span class="sxs-lookup"><span data-stu-id="4254b-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="4254b-126">系統群組包括管理員、開發人員和來賓。</span><span class="sxs-lookup"><span data-stu-id="4254b-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="4254b-127">您無法建立或更新系統群組。</span><span class="sxs-lookup"><span data-stu-id="4254b-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="4254b-128">[外部群組] 是來自于 Azure Active Directory 等外部身分識別提供者的群組。</span><span class="sxs-lookup"><span data-stu-id="4254b-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="4254b-129">這個參數是選擇性的，預設假設是自訂群組。</span><span class="sxs-lookup"><span data-stu-id="4254b-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System, External

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4254b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4254b-130">CommonParameters</span></span>
<span data-ttu-id="4254b-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4254b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4254b-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4254b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4254b-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4254b-133">INPUTS</span></span>

### <span data-ttu-id="4254b-134">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4254b-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4254b-135">System.object</span><span class="sxs-lookup"><span data-stu-id="4254b-135">System.String</span></span>

### <span data-ttu-id="4254b-136">ApiManagement 為 Nullable "1 [PsApiManagementGroupType，，ServiceManagement，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））））</span><span class="sxs-lookup"><span data-stu-id="4254b-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4254b-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4254b-137">OUTPUTS</span></span>

### <span data-ttu-id="4254b-138">ServiceManagement. PsApiManagementGroup （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4254b-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="4254b-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4254b-139">NOTES</span></span>

## <span data-ttu-id="4254b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4254b-140">RELATED LINKS</span></span>

[<span data-ttu-id="4254b-141">AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4254b-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="4254b-142">移除-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4254b-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="4254b-143">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4254b-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


