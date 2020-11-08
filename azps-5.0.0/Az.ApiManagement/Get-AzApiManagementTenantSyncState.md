---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137913"
---
# <span data-ttu-id="85d4c-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="85d4c-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="85d4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="85d4c-103">取得設定資料庫與 Git 儲存庫之間最近同步處理的狀態。</span><span class="sxs-lookup"><span data-stu-id="85d4c-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="85d4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="85d4c-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85d4c-105">說明</span><span class="sxs-lookup"><span data-stu-id="85d4c-105">DESCRIPTION</span></span>
<span data-ttu-id="85d4c-106">**AzApiManagementTenantSyncState** Cmdlet 會取得設定資料庫與 Git 儲存庫之間最近同步處理的狀態。</span><span class="sxs-lookup"><span data-stu-id="85d4c-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="85d4c-107">示例</span><span class="sxs-lookup"><span data-stu-id="85d4c-107">EXAMPLES</span></span>

### <span data-ttu-id="85d4c-108">範例1：取得最近同步處理的狀態</span><span class="sxs-lookup"><span data-stu-id="85d4c-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="85d4c-109">這個命令會取得設定資料庫與 Git 儲存庫之間最近同步處理的狀態。</span><span class="sxs-lookup"><span data-stu-id="85d4c-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="85d4c-110">參數</span><span class="sxs-lookup"><span data-stu-id="85d4c-110">PARAMETERS</span></span>

### <span data-ttu-id="85d4c-111">-內容</span><span class="sxs-lookup"><span data-stu-id="85d4c-111">-Context</span></span>
<span data-ttu-id="85d4c-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="85d4c-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85d4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d4c-113">-DefaultProfile</span></span>
<span data-ttu-id="85d4c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85d4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85d4c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d4c-115">CommonParameters</span></span>
<span data-ttu-id="85d4c-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85d4c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d4c-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="85d4c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d4c-118">輸入</span><span class="sxs-lookup"><span data-stu-id="85d4c-118">INPUTS</span></span>

### <span data-ttu-id="85d4c-119">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="85d4c-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="85d4c-120">輸出</span><span class="sxs-lookup"><span data-stu-id="85d4c-120">OUTPUTS</span></span>

### <span data-ttu-id="85d4c-121">ServiceManagement. PsApiManagementTenantConfigurationSyncState （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="85d4c-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="85d4c-122">筆記</span><span class="sxs-lookup"><span data-stu-id="85d4c-122">NOTES</span></span>

## <span data-ttu-id="85d4c-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="85d4c-123">RELATED LINKS</span></span>